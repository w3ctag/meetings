## W3C Technical Architecture Group face-to-face
### - DRAFT -
### April 23 2015

### Contents

* WebRTC update
* Future TAG f2f Meetings
* Telcon Time
* Private Browsing
* http and https, part deux.
* Web Components
* Spec Reviews

[#tagmem IRC Log from this day](http://www.w3.org/2015/04/22-tagmem-irc)  
[Agenda](https://github.com/w3ctag/meetings/blob/gh-pages/2015/04-sfo/agenda.md)

*Present:* Daniel Appelquist, Hadley Beeman, Tim Berners-Lee, Yves Lafon, Travis Leithead,  Peter Linss, Mark Nottingham, Alex Russell, Yan Zhu

*Special Guests:* Mike Smith, Cullent "Fluffy" Jennings, Tantek Çelik, Dimitri Glazkov

*Chairs:* Dan Appelquist, Peter Linss

*Scribes:* Yves Lafon, Mark Nottingham, Travis Leithead

### WebRTC update

Travis: No big news. Discussion about rechartering.

DKA: there is a new charter proposal https://cdn.rawgit.com/w3c/webrtc-charter/revision/webrtc-charter.html

Mike: Were the technical differences documented somewhere?

Travis: yes, and there are interop issues as well

Mnot: if there are interop issues at the protocol level, maybe it should be dealt with at the IETF level.

Mnot: there are issues around privacy no?

Travis: the spec requires a level of anonymity when the device is read.

DKA: If there are underspecified stuff or interop issues, there might be a need, and we might help.

Hadley: Why WebRTC didn't take off (ie: why isn't it fully mature?)

DKA: I see it taking off, there are more and more services using it

Mike: the issue is that there are no implementations from MS or Apple.

DKA: talking to people working on an implementation, they are working on a "jQuery-like library for WebRTC" .

Mike: The interesting side is that it's peer-to-peer.

DKA: I don't know any service using this for flie sharing.

Mnot: if would be good to gather more information before stepping in this.

Alex: The TAG got a discussion with WebRTC and ORTC people. It seems that the back history of the low-level vs high-level is a source of the issues.

API design, codecs, legacy interop, IPR etc... The plan was to move to 1.1, a plan that looks viable.

(discussion about the potential uses of the data channel)

Travis: the spec doesn't define the discovery of endpoints.

(discussion about the possibility of having a URL for the data channel)

[fluffy joins]

Fluffy: there is agreement on the 1.1, but there is disagreement on deprecating 1.0.

DKA: I wasn't aware that deprecation of 1.0 was part of the discussion.  
Summary of the FOs: http://lists.w3.org/Archives/Public/public-webrtc/2015Apr/0001.html  

mnot: what could the TAG do to help ?

Fluffy: the real point of disagreement is about the deprecation of 1.0, apart from that, having a clear explanation of where the disagreements are would be helpful.

Travis: The low level is getting lots of traction.  I think ORTC is the way to go, and that is what should be implemented and written down.

Fluffy: +1 all around.

### Future TAG f2f

(discussion about Extensible Web Summit, TAG events, etc...)

mnot: it would be good to change the Extensible Web Summit name, as it's not speaking to some people in the targeted audience.

Future Meetings  
- July 15-17 - Berlin
- Sept 14-16 Boston (MIT)
- Sept 17 - Summit
- October 26-30: TPAC - room for Monday AM / Friday PM
- October 31: Joint W3C-IETF Leadership meeting
- Jan 19-21: Melbourne + evening meetup
- March 29-31: Brasil / Paris - summit
- July 26-28: Paris / London - summit? 

### Telcon time

RESOLUTION: time changed to Wednesday SFO 1pm / BOS 4pm / LHR 9pm / NCE 10pm / MEL 6am (thu).
next telcon cancelled, next telcon  Wed may 6th (7th in Australia)

### Private Browsing.

DKA: is there agreement that it is a good idea?

Mnot: the goal is more framing, documenting the complexities around the concept as the first step.

Hadley: Your plan is ot use this to springboard a WG?

Mnot: not at this point. Next step is to document the current state of play.

Hadley: so coming to an understanding of what needs or not to be standardized ?

Mnot: yes.

DKA: Having different behaviour amongst browser is bad about raising awareness on what private browsing is.

Mnot: there are people in browser community with deep knowledge of the issue, we absolutely need to engage them.

### http and https, part deux.

Yan: See http://discourse.specifiction.org/t/is-https-everywhere-harmful/821  
description of the different use cases.  

1. A website with lots of historical content, http links going outside and lots of incoming http links.
2. A site 'A' importing icons and style from site 'B'

mnot: the issue is mostly deciding to load or not load mixed content, from an user-experience standpoint.

DKA draws a picture on the board where 'foo' import things from 'bar' and 'baz' -> 'foo' can't upgrade to https without 'bar' and 'baz' doing so as it would not work bevause of mixed-content blocking.  
There is a dependency graph required for upgrading to https.

Mnot: I would like to see numbers on how much imported content through img/script/style/... compared to `<a href>` links

DKA: for blogs, lots of people are embedding images.

Plinss: Mixed content handling has to be done differently if you are:

1. using https where you *want* security, so blocking mixed content make sense
2. using upgraded http, where you want to see mixed content, and flag the content as being insecure.
    
Yan: 2 ideas to service the "blg blog" community

1. don't throw a mixed content warning in certain cases (e.g. referencing an external image) but then don't mark the page as secure
2. use CSP to upgrade the connection (in the browser) but don't require CSP headers

Opportunity to discuss further in Berlin - focused discssion on this topic. In the mean time work on refining our proposals.

Tim: Is http://w3.org the same as https://w3.org ?  What Brad has said is "no".

Alex: what he has said is that they have different guarantees.

Tim: From most perople's point of view when you're linking to something the interesting thing is the thing (e.g. json file of weather) - and the security you get it with is incidental.

Mnot: In SW is there a notion of the trust level assigned to a particular statement or triple?

Tim: There's a whole provenance discussion – e.g. used in science – tracks data and where it came from. My software keeps the headers. MOst time it ignores the headers but sometimes it uses them.

Mnot: anything that takes account of hsts?

Tim: nothing.

Hadley: behavioural perspective: 
    
Yves: hsts is timed - it can be renewed. You need to have a way to add in the model statements that are timed.

### Web Components discussion with special guest: dimitri!

dimitri: I'm a repeat visitor!  
… it was more than a year ago.  
… Dimitri v2 now.  
… Reflecting back on the last year:  

1. Several classes of features on the platform. Those that have networking components are hard. Incremental features are somewhat easier (can get opt-in usage).  
Web Components are a network-effect kind of feature. It redefines DOM, HTML, and is \_complicated\_. It's a heavy burden to bear (er... get implemented)  
Expectations for adoption need to be adjusted (probably lengthened)  
Cost of Web Components--it can only be hyped for so long before folks come back to reality due to lack of browser adoption.  
I would like to fix how this works (in my next lifetime)

2. Finding the primitives, rationalizing existing behavior also seem like good ideas.... I'm optimistic! about the upcoming f2f tomorrow. All vendors understand and have vetted their concerns  
… I'm hopeful we can now drive to consensus which should lead to browser implementations.  
… Proceedurally: I would like to drive a 'task force' style of editing. Designate folks to take specific features and mold them.  

Lets us divide and conquer and also get cross-vendor help.  
Still lots of work to do. Spent some time triaging web components bugs this morning.  
Last 5% of interop is the hard part. The edge cases are what really generate sadness for web developers.  
(I think we need to do the same for various other specs.)  

Alex: The accessibility + custom elements discussion sounded like we haven't fully explained how the HTML elements in the platform work.

dimitri: Sitting down with folks; have realized there are lots of things "bolted into HTML elements" (TM).

* Most things that look like a button on the web are actually divs. 
* `<sad face>` for accessibility

Tantec: perhaps the button only works for 90% of the time where the div is 100%.

dimitri: Date picker is another example where things are very different between implementations
… there will be multiple actors across web components, but accssibility wants to apply behavior globally!!

dka: One of my hopes for web components is to make things more coherent for developers.  
… Right now the story is mixed and fragmented by various polyfills, etc.

dimitri: Taking a tangent...  
… The "multiple actor problem" (or "software engineering").  
… This is very pronounced on the web. Cite: "Disqus" you can add a little JS and get comment support on your web page! Cool, right? The immediate impact is that your web app is slower.  
… Hmm, how to solve this? Lazy Load!, hmm, when to load? Hook the global scroll event!! Spirals out of control... (and a great way to have non-indexed comments on your pages. Also note prior art/site "Haloscan" which did the same thing, but was shut down 2009-12-29, taking all of its centralized hosted comments with it. -tantek)

dimitri: I want to enable these kinds of apps. I want to do it by solving the coordination problem.

dimitri: Web components tackles the composition problem; "how do I allow multiple actors to work on a page without stepping on each other?"

dimitri: This is the next problem we'll be tackling - the coordination problem.

dimitri: E.g., requestAnimationFrame. If you trace sites that rely upon it, most of them blow their budget in that function. 

dimitri: Our API provided this hook to create this endless train of tasks, but we didn't give the developer a way to observe the length of the train or hint how important tasks are.

dimitri: Simple impact of coordination problem is jank; sites don't look/behave as awesome as native.

dimitri: Something other than components will solve the coordination problem.

Alex: When you have traced big apps that use shadow DOM, that has helped to resolve some of the coordination issues?

dimitri: yes. Shadow DOM is a style isolation boundary. You can parallelise style resolution, unless you use a shadow peircing combinator. Unfortunately, they're like crack; they're evil.

dimitri: We have to be very cognizant of this. There isn't understanding in the world of these two problems. Framework authors have solved the combination problem --

Alex: Inside their frameworks.

dimitri: yes. 

dimitri: Some frameworks have put the coordination problem as a front-line concern; e.g. react. They do this because they gain ergonomic and performance benefits. 

Travis: also Require.js.

dimitri: yes.

dimitri: From a TAG perspective, it's an interesting challenge in terms of how you talk to devs, because it doesn't affect you when you're first starting; it's when you add libraries/scripts at the last minute, and suddenly perf goes to crap.

dan: Last year, when we were talking about promises, Domenic wrote a promises guide aimed at spec writers. Would it be useful for us to think about writing something along these lines?

Travis: yes.

Dan: action to Travis :)

dimitri: Accessibility is one of those actors that really does want to see a global perspective. I don't know how to reconcile this. Could you solve this by saying there is only one top actor? 

dimitri: With power comes responsibility :)

Alex: It doesn't seem like there's anything on the HTML WG's plate to explain how its built-ins are constructed. This is a persistent request; e.g., for customisation of input elements, for accessibilty. We've had multiple conversations this week about this. We don't have any mental model for what happens when you type a keystroke. Is it our job to ask the HTML WG to address this? Is there some other group?

Travis: Who else would do that other than HTML WG?

Tantek: If it's presentation, CSS. That's I guess a big source of bugs and frustration. E.g., for styling input elements.

Alex: Is the implicity shadow DOM of a built-in enough to customise it?

Alex: If I can name part of a built-in element, like a select element drop down, and style that independently, how would I expose that to third parties?

Travis: Of the hundreds of algorithms in the HTML spec, how do you make those things a) true, and b) available to something that participates in the process (e.g., accessibility)?

Travis: How do you get the push effect of a button, focus model, global tab state, etc.?

Peter: the button is the simplest one. We have this in CSS: e.g., the :focus pseudo-class. It gets more contentious with anything more complicated than a button.

Peter: there's no interop between browsers, and little consensus that there ever will be, because of new platforms

Travis: e.g., file upload has changed over time.

Alex: When you start to customise via CSS, you get a default version. That default also isn't specified.

Peter: Some are; e.g., in the UA stylesheet. Not always true.  It's been contentious as to whether they should be styleable. 

Alex: It sounds like there's a real tension there. The WG and browser vendors are the only ones that have had a say.

Peter: The CSS WG doesn't have power over implementation of the form controls. It's a black box within the CSS black box.

Dan: I assigned an action to Travis to explore a TAG best practices here, it might align with your existing work. This feels like it should be documented somewhere.

The original set of Web Components proposals included something called *Decorators*  
[“A **decorator** is something that enhances or overrides the presentation of an existing element.”](http://www.w3.org/TR/2013/WD-components-intro-20130606/#decorator-section)  
[HTML as Custom Elements](https://domenic.github.io/html-as-custom-elements/)  
[HTML as Custom Elements repo](https://github.com/domenic/html-as-custom-elements)  

peter: If we could style form controls, how would we expose that to custom elements? The way we were doing this historically, we exposed style through pseudo-elements; i.e., you expose bits that can be styled. There have been proposals to give that capability to custom elements, rather than shadow piercing. The consumer won't know if they're dealing with a web component or a built-in.

Alex: It doesn't resolve the question of "I'm trying to achieve the same level of styling" -- it would be assured by a compatible styling system with compatible DOM layout.

dimitri: This is the network effect style change; until every browser does it, and it's in the wild, it won't be used.

Tantek: unless you define a fallback.

dimitri: yes, but that's a big constraint.

Alex: sometimes the native element doesn't fit all uses, and a replacement could be better handled by frameworks.

### Spec Reviews

[API reviews](https://github.com/w3ctag/spec-reviews/issues/)

Daniel: More spec reviews that aren't on our list?

Spec- document.scrollingElement  
* Different browsers use different elements as the root scroller.
* The API returns which element is the root scroller
[discussion about how CSS creates/manages scrolling region vs. viewport, who in CSS has reviwed, etc.]

Spec Proceedure  

Daniel: Is it OK to just open an issue in the repo?

Group: form to provide: timelines, security review, discoverability of the form, documenting the process.

Alex: we should our spec issue tracking in one place (Github if at all possible). (this might be an option: http://issuetemplate.com )

Spec Review: Permissions API (https://github.com/w3ctag/spec-reviews/issues/45)

[live-editing of the spec rewview issue list in github as we discussed each review]    

