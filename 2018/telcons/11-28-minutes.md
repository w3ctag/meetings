## TAG Teleconference
##### 27 November 2018

Present: Peter, Kenneth, David, Daniel, Hadley, Yves, Alex, Lukasz

Regrets: 

Scribe: Kenneth, Dan, Hadley

---

Agenda:

* JS Modules and Feedback from Node Community - do we need an issue?
* [Background Fetch](https://github.com/w3ctag/design-reviews/issues/279) - @slightlyoff @kenchris @travisleithead
* [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) - @slightlyoff
* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff @dbaron
* [Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134) - @cynthia @torgo @travisleithead
* [`sec-metadata`](https://github.com/w3ctag/design-reviews/issues/280) - @slightlyoff @dbaron @hadleybeeman @plinss
* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297) - @torgo @hadleybeeman @travisleithead
* [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282) - @cynthia @kenchris @travisleithead  
* [HTML General Review: Web Sockets](https://github.com/w3ctag/design-reviews/issues/268) - @slightlyoff @ylafon
* [Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/235) - @slightlyoff @dbaron
* [Should WebRTC be [SecureContext]](https://github.com/w3ctag/design-reviews/issues/228) - @travisleithead @cynthia
* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) - @cynthia @plinss
* [Serialization of natural language in data formats such as JSON [I18N]](https://github.com/w3ctag/design-reviews/issues/178) -  @cynthia @dbaron @travisleithead
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62) - @slightlyoff
* Call time - what is it good for?

---

David: regrets for next week

### JS Modules and feedback from node community

Dan: I think the consensus was that probably nothing we can add to this... but just wanted to check up on it since I got some feedback... from npm people who, despite isseus with recent exploits in npm -- i wanted to see what to do.

kenneth: I'll follow up today.

dan: I think our main issue is that people who have a lot of sunk cost into the way that modules work in node are feeling like they're being cut adrift by es6 modules. This feels to me like helpging them would be good. Is that happening?

alex: I think there is a constraint set of options; there isn't an unexplored area. You end up with a mechanism to identify modules by filename or by parsing them. es6 modules don't have an easy way of declaring themselves that. Because node has a proprietary import mechanism, it's not clear what to do.

kenneth: and the standard can't adopt what they do now, becasue it would kill  performance.

alex: Yeah, we did this in 2006... you could never use this on the web. Most of this is around deplyment, because very little javascript is run on the server as opposed to the client.

[discussion of what node does today vs. ES6 modules approach]

alex: Beyond what the node community have tried to do, what is left? Everyone understands the technical issues; not much to be done socially. What can the TAG do?

kenneth: exactly. the boat has sailed; we just have to make it work with es6 modules.

dan: is there any work going on to reduce the amount of pain for people to migrate?

kenneth: import maps... closer to feature parity. You can define how to resolve the modules, hte fallback chain, shortnames etc. Different solution to node modules, but I think it's better.

dan: I feel like there is a lot of decentralised discussion and uneven distribution of knowledge. Could we do a blog post or something? Or someone else, and we suggest -- to defuse the issue? 

alex: Yeah, node is learning that they did it wrong. They're going to have to move, and that's not fun. That were consulted at length in the es6 process, which sometimes was good and some not. Important: npm has a priviledged position in the ecosystem. They have global knowledge of what can be es6 or just classic modules. they could solve this with software

kenneth: yeah, they could preparse all the modules on the servers.

dan: okay, maybe we should keep the dialogue open with them.

kenneth: import maps... explainer on github. https://github.com/domenic/import-maps

### [Background Fetch](https://github.com/w3ctag/design-reviews/issues/279)

Alex: ...

kenneth: Why couldn't this be the metadata to the map?  

David: i don't understand why ... this design.

Alex: so sitemap.xxx for modules?

kenneth: Seems to be other things for metadata you might need for your modules.

Hadley: if there is a bottleneck ... explainer says - this is a problem, this is the solution. Does not explain why or what else was considered.

Alex: I think it's a good point.  I will go back and talk to the requestor's manager.

David: I was also starting to write a comment - i'll add that.

kenneth: how would you ensure integrity? that would be nice to have in your module map.

David: https://github.com/w3ctag/design-reviews/issues/213#issuecomment-442335197

### [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) 

David: some of this was to remind me to do stuff and i haven't done the stuff yet.

Peter: [bumping 2 weeks]

Kenneth: BTW this just landed in safari tech preview https://bugs.webkit.org/show_bug.cgi?id=159475

David: we just got a [separate review request](https://github.com/w3ctag/design-reviews/issues/328) for v2.

### [Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134) 

[bumped a week]

### [`sec-metadata`](https://github.com/w3ctag/design-reviews/issues/280) 

Yves: Mnot posted a blog post on how to design http headers optimised for hpack - https://www.mnot.net/blog/2018/11/27/header_compression

Alex: what is the overall header bloat issue - what is the budget?

Yves: i think it's a separate issue - not related to sec metadata in itself.  I suggest asking mark or others in the http working group we can ask this.

[closed]

### [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297)

hadley: looks like we are discussing tangents .. mike has said 28 days ago that it will be more clear when he writes a spec. suggest we close it and say "great, see you then."

Dan: I agree.

Hadley: I will close.

### [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282)

Alex: argument is that pieces are welded shut because that's a good thing. i'd like to see the data. I'll respond

Kenneth: [related to]... transform streams?

Alex: it's all very wired shut

Kenneth: the transport stream is more like an interface.

Alex: it's not clear that you'll get the same behavior - generating new streams out of existing streams... what s is the delegation mechanism...

Yves: what is the default encoding of streams in javascript?

Alex: ...

Alex: you can't just make a transform stream...

[...discussion on what feedback to leave...]

Alex: https://streams.spec.whatwg.org/#is-transform-stream

David: if there are issues with transform streams it's worth raising them.

Alex: i'd like to make this less magic. Will leave feedback.

### Call times

David: the 3 things - each of them could become a perm call time. the problem is that it's hard to make it work for both sangwhan and travis. 

[nothing changed for now]
