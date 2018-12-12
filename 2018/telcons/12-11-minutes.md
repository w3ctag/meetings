## TAG Teleconference
##### 20 December 2018

Present: Peter, Kenneth, Yves, David, Travis, Hadley

Regrets: Lukasz, Alex, Sangwhan

Scribe: Travis



---

## MathML

* [MathML](https://github.com/w3ctag/design-reviews/issues/313) - @cynthia @slightlyoff @dbaron

David: (paging this back in...)

Travis: Saw a note about this at TPAC (Igalia was going to implement).

David: This is implemented in Gecko.

Peter: Let's defer until we have Sangwhan

## Clear Site Data 

* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62) - @slightlyoff

PL: Passing because we don't have Alex.

## AOM

* [AOM](https://github.com/w3ctag/design-reviews/issues/134) - @cynthia @torgo @travisleithead

Travis: We've provided some good feedback already--and it's been received.

KC: Also talk at TPAC around Searchable Invisible DOM and Display Lock... etc., need to understand how these relate.

Travis: propose to close it? We can open a new review with more concrete AOM specs to look over...

Peter/KC: works for us.

## Serialize Natural Language

* [Serialization of natural language in data formats](https://github.com/w3ctag/design-reviews/issues/178) - @cynthia @dbaron @travisleithead

David: Perhaps we should punt this a week (or five).

Peter: Moving to the 15th (Jan '19)

## Web Sockets

* [Web Sockets](https://github.com/w3ctag/design-reviews/issues/268) - @slightlyoff @ylafon @kenchris  @travisleithead

Travis: needs to have the issues filed in WHATWG to officially close this off.

Peter: moving to next week to review. Close as well if you'd like to.

## TextEncoder/DecoderStream

* [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282) - @cynthia @kenchris @travisleithead

KC: Alex's comments have been responded to... Not super-clear on how the generalized transformStreamController would benefit web devs... May need Alex to weigh in.

KC: It is fine that you can inherit from TransformStream, but no example in the streams spec does that eg. https://streams.spec.whatwg.org/#example-ts-lipfuzz - added a comment

Peter: defering until we have Alex.

## MediaCap

* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) - @cynthia @travisleithead @plinss

Travis: may need Sangwhan to let us know if we've reached the bottom of this review.

Peter: sounds good; defered.

## Intersection Observer 1/2

* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) -  @slightlyoff @dbaron
* [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) - @slightlyoff @dbaron

David: on v2, I have some concerns from a Mozilla perspective... I need to add these comments. Goal is adding features to IO so that pages can verify that a certain part of the page is visible. Use case: if not fully visible, then block from using (the feature) for click-jacking. Spec says you can't give false neg/false positive, but this coudl lead to browser interop issues (for boundaries like CSS visual overflow like blurs/shadows).

## Background Fetch

* [Background Fetch](https://github.com/w3ctag/design-reviews/issues/279) - @slightlyoff @kenchris @travisleithead

Travis: Want to read the related blog post, check on the latest text around grouping to make sure it feel good about it.

KC: Here's a related article: https://developers.google.com/web/updates/2018/12/background-fetch

Peter: coming back next week.

## CCSSSS (Constructable CSS Style Sheets)

* [Constructable Stylesheets](https://github.com/w3ctag/design-reviews/issues/308) - @dbaron @kenchris @plinss

KC: was looking for a good explainer. You define a model scope outside the element, and just use it there.

David: I'm CC'd on a bunch of issue--note one about 'switching back to real constructors'.

David: Cloning may seem interesting, but then you don't want to duplicate.

KC: shadowRoot.adoptedStyleSheets would like to see an example in the spec (to show how it's supposed to be applied/used).

Peter: 'disallow modification flag' ?

David: For the async case--seems to be only set during that async part (also applied in the sync algorithm on in/out).

Peter: OK. To prevent modification during the async operation.

David: If an import fails to load, it leaves this flag set (need to file an issue on this--just discovered).

Peter: otherwise, we're happy with this?

KC: yep.

Peter: Folks, please file your issues, then we can close.

## Bonus material

Agenda+ RTC over WASM: see https://youtu.be/gV354kWh08o?list=PL4_h-ulX5eNfaM0QM5r-PewWaY_zgLH7b&t=1226

Hadley: isn't that inefficient?

David: there's a lot of things in PeerConnection that are provided that may not be available?

Travis: this made me uncomfortable

David: Much of what we do allows the browser to act as the user's agent. This depends on various features being implemented (or having hooks) in the browser. Permissions, etc. Some web content has to be written in a high-enough language that we can reason about it.

Hadley: even if we can reason about it, it takes away the user agent part of the web (the context the user is used to having control over, and instead puts it under control of the server).

Travis: So, what's the API boundary that is necessary?

KC: WebIDL bindings can allow you to go straight from WASM to C++... Thinking about exposing existing things through modules... Not it seems exposing some things to WASM that might not be exposed to JavaScript (like POSIX APIs). We perhaps don't want to create a parallel browser.

Also thinking about WASM runtimes outside of the browser. Looking to have built-in APIs.

We shouldn't ignore this; want to make sure that there is API alignment.

David: Related... one of the things with WASM (stuff exposed to JS is hard to get at through WASM), ES Modules, provide a better interface to WASM. So, certain new API can be bundled in a module. So, building a standard library would be nice.

Peter: can you file an issue on this for tracking?

Travis: Yes, I'll file it.

---



