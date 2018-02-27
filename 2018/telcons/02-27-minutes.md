## TAG Teleconference
##### 27 February 2018

Present: Peter, Hadley, Sangwhan, Dan, Lukasz, David, Alex, Andrew, IanK (Guest)

Regrets: Yves

---

Agenda:

* [CSS Layout API](https://github.com/w3ctag/design-reviews/issues/224) - Dan, David, Travis - Guest IanK

IanK: (Gives an intro to the API, presenting the [explainer](https://github.com/w3c/css-houdini-drafts/blob/master/css-layout-api/EXPLAINER.md))

...I'ts part of Houdini, does for layout what...

Example: Pinterest has a layout with tiles cascading down the screen. Not ideal for performance, doing it with scripts. 
We see constraint-based layouts with native platforms. Also a lot of demand for more control over how text gets laid out. Example: CSS Shapes spec.  There is shape-outside which allows you to flow text outside an arbitrary shape. You can see that with CSS shapes (interruption)

One way to do this is with the CSS layout API.

A lot of the spec is a bit foreign.  CSS we typically think of elements having width and height, top right. IN CSS they are inline sizes and block sizes. (shows mapping).  So out of the box the API will work with different writing modes. Standard CSS layouts work in this logical mode. Doesn't make sense to have his only work in physical coordinates.

Next: a new worklet alled the layout worklet.  You give it script to execute. Once that promise resolves, it says "this layout is ready to use."

The real guts of the API... jumping between the explainer (which isn't updated) and the spec. In a layout worklet, you can register a layout. You give it a name, in this case 'centering'.  I don't think we're going to extend the layout anymore. The function is this layout fucntion. This gives you a list of your children, your current style, what we now call layout constraints, and edges.  Edges are what the default scroll bar border padding are. 

Alex: Are edges expensive to compute? We talked to Alex T about this on resize observer.

IanK: working out the boxes might be expensive.

Alex: He's handing us a box, for resize observer. 

IanK: the border box is super cheap. What he might be referring to here is that you need to do some extra calculation to work out the other boxes.

Alex: So it's not onerous?

IanK: No.

... Most useful thing in edges is edges.all.  

...We've got the styleMap here, the same as for the paint API. when you perform a registered layout, you need to specify ahead of time whta the input properties are. Internally, we use this to invalidate the layout of these properties.

Alex: So the person specifying the properties is the author of the class?

IanK; Yes

...On to Child input properties.

Alex: Can they be any property or just the custom ones that are passed in?

IanK: Any. If you want a grid layout...

...Here's an example of grabbing the child input properties. Any time the child property bar changes, it will invalidate the layout.

...The next argument is the children, which is just an array of children for the layout. The only useful thing you can do is ask them to perform layout. 

...Questions?

(no)

IanK: We also have layout constaints. Like how much available space there is, if you've been forced to be a prticular size. to allow for fragmentation to occur.

Alex: That seems quite important.

IanK:  It's hard for an engine to support this initially. Edge and maybe Firefox will have an easier time of this than we will in Chrome. A lot of the inspiration was taken from Edge.

...Explainer is slightly out of date but useful for shoing how layout works.

...Purpose of layout: you get back layout children. You get a childFragment, which you can position anywhere.  Here you can see the web dev layingout a child and producing a fragment.  You give it a set of constraints (width/height, or 100px by 100px, etc) as we do in grid and flexbox layout. and from that you get a child fragment.

...Questions?

alex: For each of these, you accummulate a size? 

IanK: in this example, which is a bit contrived — layout called centering — is not invalidating on any properties. It's looking through all the children, working out the maximum size of the children (which you don't need), grabs the fragments, and then positions them in the centre. 

alex: inline offset and block offset.. from left and top?

IanK: yes.

alex: that's a big confusing.

...I have a question on 6. It looks like it's an instance of something — that you had elsewhere — that you don't make constructable and you don't use here. ??

IanK: You could have a constructor here, but a lot of validation needs to happen by the engine to produce a fragment. For example, if you are turning in inline size, and the engine knows you have a fixed inline size, the engine knows it has to invalidate that.

alex: how does the engine know that?

IanK: Happens with input constraints.  

Also, childFragments need to have consistent break tokens.

alex: so how does someone writing layouts discover these constraints?

IanK: they are passed as part of the layout object.

... and you can enforce constraints on your children as well. 

alex: I'm trying to understand whose respnsibilities are whose.  

IanK: Broadly speaking, it is your responsbility to give your children a set of constraints and perform layout on them. Once you get back a fragment, it's your responsibility to position them.  You can ask the engine, "I want to be this block size", but it can override you because of the constraints.

alex: I want to play with this to make sure the names make sense.

IanK: It's how all the engines work internally. WE have to harden this, because the engines don't have clear responsibility of who is responsible for what. For us, in certain circumstances, it's the child and in others the parent who is responsible for specific sizes. So we're teasing this all out.

It's going to be difficult to make interoperable from day one. But we'll see.

Alex: seems like there is an argument for validation here. You're half in the type system, which is a bit weird. I can see a coertion where where you implictly convert. I'm happy for it to reutrn the bag, but I'd love it if you could construct a fragment, you could validate it.

IanK: Initially, we might make it in chrome that if you have n layout children, you have to return n fragments. We can't just do 5 of the 10, for example. 

plinss: When you have a bunch of children adn can't make them all fit, can you say you can only handle this many, and something else needs to take over the rest...

IanK: Yes, that's in fragmentation. I don't think chrome can do that easily, but we want to.

...To explain text fragmentation:  It's a layoutChild which usually returns one fragment, a box of width and height. Text produces multiple fragments (think: one per line).

...It's relatively common. Chrome shoudl add it after the initial implementation. Things can also fragment in the block direction. This is how CSS multi column works. Currently, engines do this in wildly different ways.  We've all agreed to do text fragmentation in the same way... but it'll be a while before we get there.

dbaron: You mentioned fragments having to be right? That made me wonder... do the fragments internally know which child they were for?

IanK: Yes.  Internal fragment representation knows... it has a pointer to that layout child.

dbaron: good

ianK: At least initially, super important: text fragmentation. Then, block fragmentation to do multicolumn or regions.  We're prioritising by what should be most useful.

...Scrolling: handled by the rendering engines differently. We want to support autoscroll bars initially. If you overflow, layout can be invalidated. We're handling that in the edge object. Precomputed scrollbars.  

Alex: Are there other situations in which you might get it recalled through the process?

iank: yes.  This is an interop issue, and we're wildly variant on when we'll call a layout. And we have different invalidation logic. The way that engines use intrinsic sizes... from what I know, differs too. Some engines will perform layout when computing intrinsic sizes.

...This is one simplification we may want initially. Jumping to hte simple centring layout — you get to compute your inlineSize and blockSize. Intitially we may want — the engine always forces a size on you. You get to return an auto blockSize (the height of an element with 0 constraints).  That simplification of the API will reduce some power but will gain a lot of interop correctness.

david: does that prevent it from doing sizing based on the content?

iank: Yes. Not covered here is the intrinsic sizes callback — where you have that sizing-to-content hook. But not the full power.

alex:  This is fundamental to CSS?

ianK: Most engines don't have this. they do it through the intrinsic sizes callback. Most layouts don't size based on their content.

dbaron: I should follow up with you on this.

iank: I've implemented this behaviour in our prototype implementation and it works. Takes complexity from the API. In future: hope we can get to where yo ucan say "I don't want you to force any size on me."  A flag for that.

...You use this by the display property.  

`display: layout(centering);`
  
...Another thing implicit here: overflow is handled for you, when you need that. You can't allow that now because the engines aren't interoperable right now.  Based on bugs that we know about.  In some cases, margins overflow differently on different engines.

...So, long term, we'll say overflow is produced by the layout.  Initially, we'll say whatever engine you're running in will compute overflow.  CSS has a lot of interop issues.  But hopefully this all will help us converge.

...Another quirk of the API right now: most contentious thing. The layout function is a generator.  intrinsicSizes is also a generator.  Most engines are synchronous, but some are implemented in this generator style. This is the first time this pattern is used in the platform. Alternative is to do this promise-based. Cons of promise-based API: not a strict API surface. other promise-based APIs that go into the JS stnadard library; we want to keep this function synchronous and don't want to wait on something like a dynamic import. We're not sure of performance differences between promise-based vs generator style... this area is open to debate.

alex: Argutment for the genrator style?

iank: the clamping of the time. Might be quicker on the bindings as well. not showing here you can return an array, so less hops back and forth between the javascript and the generator. Might be faster; needs testing.

...We expect this API in particular will be super dependent on how fast bindings performance is. My main point of view: keep it as generator-style. No interactions with other promises. 

...We choose those two styles because engines like Servo might do this work on a completely different thread. 

...Happy to hear thoughts.

Alex: Next step?

Iank:  i'm implementing a subset of this API in Chrome. I've got basic demos; should be able to layout children by end next week.  I'm going to clean up explainer first. We have a Houdini F2F in April; issues to work out there.  My hope is that what is implemented in Chrome, should be able to ship the rest by second half of this year.  Whole API surface: 3-4 years.

...With it, you'll be able to do all the blocky type layouts. High fidelity flexbox or grid layout, constraint based layouts and masonry layouts.  Anything where your layout is trying to control things on a box level.  Next most useful: line fragmentation part of the API, but that's not in the initial work. From that you should be able to do complex text following around objects, etc.

...You should be able to do a high-performance implementation of the container query, which I'm excited about. Example: polyfill gridLayout, but say what the grid template areas are. 

dbaron: I'm concerned about doing that at layout time.  If that's something done within the layout system, it implies changing the intrinsic sizes in a way that means they don't behave in a reasonable way.

ianK: that will be up to the web dev, their intrinsic sizes. They may have to lie, or learn not to overconstrain it.  A lot of people will return "interesting" intrinsic sizes with this API.

Hadley: isn't that counterintutive? Confusing?

ianK: Yes, this is a worry with all Houdini work. You will have some doing that, writing unintuitive layouts.  We'll have to see what happens; not sure how to protect against that.  I don't have a good answer there. 

alex: it's like them returning bad resources out of a service worker.

plinss: Yeah; don't help them.

ianK: I expect that people will implement a container query grid or flex layout based on whatever fixed layout size they get given... they'll have to deal with the bugs. Comes with the territory.

plinss: Goal: let people efficiently do what they're currently doing very inefficiently with scripts and horrible DOM manipulation. Examples?

ianK: I'm not sure if you can do something like grid CSS with this. Container queries will be another. I also expect we might see people trying to do a faster block-like layout based on this API. Here (shows example). 

plinss: thank you very much. Any other questions from the TAG?

iank: I'll check back in in about a month. 

---

alex: I do want to talk about accept-CH; I spoke to Ilya. Learned that we're all frustrated that this isn't enabled for top-level resources. Their idea has been to get this launched and then see if they can make a case. All engines seem split between users and network containers, who are concerned about header size. We also don't have a clear answer for what is "too much".  It's now 14k as opposed to 4. Seems like Ryan Sleevi and Patrick McManus are the ones we should engage with, re why not to send this up front.  Next step: write this up in general, esp re top-level documents.

andrew: Seemed like that was design goal?

alex: More pragmatic.




* [CSS Typed OM](https://github.com/w3ctag/design-reviews/issues/223) - David
* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - David
* [Img decoding attribute](https://github.com/w3ctag/design-reviews/issues/220) - David, Sangwhan

Sangwhan: No external feedback so far.

* [Web Locks API](https://github.com/w3ctag/design-reviews/issues/217) - Andrew, David
* [Accept-CH header](https://github.com/w3ctag/design-reviews/issues/206) - Andrew, Alex
* [ResizeObserver](https://github.com/w3ctag/design-reviews/issues/187) - Alex, David
* [HTML Genreal Review](https://github.com/w3ctag/design-reviews/issues/174) - Alex, David, Hadley, Sangwhan, Travis
* [Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101) - Hadley, Lukasz
* ["With Credentials"](https://github.com/w3ctag/design-reviews/issues/76) - David


Backlog:

* [Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/226) - Sangwhan
* [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - Alex / Hadley / Travis / Peter
* [OffscreenCanvas](https://github.com/w3ctag/design-reviews/issues/141) - Sangwhan / David / Travis
* [Review Accessibility Object Model ](https://github.com/w3ctag/design-reviews/issues/141) - Sangwhan / Travis
* [Secure Contexts & TC39](https://github.com/w3ctag/design-principles/pull/75) - Sangwhan
* [&lt;link&gt; rel=modulepreload](https://github.com/w3ctag/design-reviews/issues/213) - Alex, Andrew
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/213) - Andrew
* [Decentralized Identifiers](https://github.com/w3ctag/design-reviews/issues/216) - Hadley
* [Web Speech API](https://github.com/w3ctag/design-reviews/issues/214) - Hadley, Travis
* [Transform Streams](https://github.com/w3ctag/design-reviews/issues/211) - Sangwhan, Alex, David
* [import.meta.url and import.meta](https://github.com/w3ctag/design-reviews/issues/208) - Alex
---



