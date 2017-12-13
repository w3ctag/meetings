TAG Teleconference
12 December 2017


Present: Dan, Hadley, Andrew, Peter, Yves

---

Dan: is there anyone in the other channel that we're not in

Andrew: &lt;unnecessary sarcasm&gt;


**Topic: WHATWG**

Dan: New governance model, rel between WHATWG and W3C


Dan: TAG has role commenting on WHATWG is doing, it would be good to strengthen that, in this new era.&nbsp; Already, eg fetch is normatively refed from W3C specs.&nbsp; Maybe we need official liaison. Since dbaron is on WHATWG steering board maybe it should be him, but I'm not nominating him.


Hadley: how is this changing the rel?

Dan: Parallel specs.&nbsp; A lot to do with IPR, lack of stable framework in WHATWG. MS has now joined WHATWG, so all implementors are there

Alex: [name] is our rep to that body.&nbsp; Four browser vendors signed on to WHATWG.&nbsp; New editors have been announced of the W3C's HTML, but none are implementors.

Alex: Changes at W3C have not been propagated, and implementors don't take any notice

Alex: This is a formalisation of the status quo

Dan: I'm worried about more stuff moving to WHATWG, if good work is happening at W3C.

Alex: Nothing new is going to move

Dan: Should we formalise TAG relationship with WHATWG

Alex: Making incubation and TAG review part of the implementors' process for shipping new features is most important, regardless of which standards org ultimately does the spec

Yves: The TAG reviewed WHATWG specs in the past, it is expected the TAG will continue to do so.

Hadley: What does WHATWG want?

Dan: There's a fight coming up about whether there's a place for W3C HTML.&nbsp; Should TAG get involved.

Peter: [shakes head]


Dan: I'm concerned about the practicality of living standards in some areas, eg government, [procurement, etc...]

Hadley: The architectural bit of this is in the risks that come with forking the HTML spec. We do have an interest in seeing that both SDOs work together smoothly. But I'm not sure we need to be involved in the details of HOW that happens.&nbsp;

Agreed: We are here to help across the web platform&nbsp;

**Import.meta (#208)**

Alex: stage 3 draft.&nbsp; Scheduled to chip in Chrome 63

Alex: will feed back on this today.

**Accept-CH (#206)**

Some concerns persist about the design

... still a mechanism where the server is expected to decalre an interest... ahead of time...

Andrew: is this a necessary thing as opposed to just sending the info in the first place?


Alex: [concur]

Andrew: I think we should push back asking them to justify [this complex solution] to an alternative approach which has no downsides. Assuming the justifications are valid, then the Accept-ch header is the worst of both worlds... and from a developer perspective it is confusion. as a developer you see accept as request headers not response headers.

Alex: I will follow up in the comments here.

**Web lifecycle (#205)**

Dan: missing Travis.&nbsp; moving on...

**IntersectionObserver (#197)**

Alex: working on v2.&nbsp; Better data on occusion

Dan: last time we looked at it we noted that timing needed a look.

Andrew: ???

Alex: The event delivery of any single event is unpredictable, but relative to other events it should be deterministic




