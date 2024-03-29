# TAG Teleconference
#### 25-27 March 2024

---

## Agenda:

### Breakout A (Europe / China) - [2024-03-25](https://www.timeanddate.com/worldclock/converter.html?iso=20240325T100000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman
* [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916) - @torgo, @matatk, @hadleybeeman
* [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion
* [Gamepad Trigger Rumble Extension](https://github.com/w3ctag/design-reviews/issues/934) - @torgo, @matatk

### Breakout C (California / Australia) - [2024-03-25](https://www.timeanddate.com/worldclock/converter.html?iso=20240325T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

### Breakout D (California / Australia) - [2024-03-26](https://www.timeanddate.com/worldclock/converter.html?iso=20240325T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Meeting with W3C Team to discuss appointments


### Breakout E

#### [Gamepad Trigger - maybe close](https://github.com/w3ctag/design-reviews/issues/933)

*bumped*

#### Discussion on Generative AI

Dan: https://www.w3.org/blog/2024/managing-the-impact-of-ai-machine-learning-on-the-web/ https://c2pa.org/, https://www.bbc.co.uk/rd/blog/2024-03-c2pa-verification-news-journalism-credentials, https://www.w3.org/TR/2024/DNOTE-ethical-web-principles-20240319/#verify

Yves: See also https://www.w3.org/TR/vc-use-cases/

*discussion on verification of information...*

Max: is there a mechanism in the design of the web architecture to do origin verification ... could be helpful to whole generative AI... so this could be related to TAG - an architectural issue... We need to do more work on what we could do here...

Yves: also the document that Dom edited - is welcoming feedback to improve it... 

-----


## Breakout A

Present: Dan, Yves, Max

Regrets:


### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Dan: *pings Diego*

### [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman

Dan: I will reach out to Chris Harrelson

Max: they promised to update the explainer to analyze unintended consequences and also the party who receives the report... but no update yet.

Dan: *leaves note on issue*

### [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916) - @torgo, @matatk, @hadleybeeman

Max: they agreed to put this on hold...

Dan: Sets to "stalled"

### [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion

Yves: diff https://services.w3.org/htmldiff?doc1=https%3A%2F%2Fwww.w3.org%2FTR%2F2023%2FCR-webnn-20230330%2F&doc2=https%3A%2F%2Fwebmachinelearning.github.io%2Fwebnn%2F

Max: I wan to mention... the author mentioned about the update for transformers... they talk about some use cases but don't find those use cases... One suggestion is to put the transformer use cases in...

Yves: the use cases has text to image, speech recognition and text generation...... Text to text transformer... It's not entirely clear... you have to infer what transformers are for... Also a few API signatures that have changed - to async using promises... But someone needs to look at the API to see if it makes sense or not.  ... looking at the IDL, it seems pretty much OK...

Dan: *reached out to Martin*

### Discussion on Appointments...

## Breakout C

Present: Matthew, Peter, Martin, Tess, Lea

Regrets:


### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk

Matthew: I think they've answered most of the questions we asked. They seem to've moved closer to the Compute Pressure API appraoch (with buckets) since our review started. Would it be useful to share the info from DAS WG about side-channel attacks with the Web Audio group?

Martin: Seems reasonable. Doesn't say how many buckets.

Matthew: They're still deciding that.

Martin: Risk is that due to things like CPU throttling, attacker can learn about the nature of your machine. Though these things tend to be high latency. This is a low bandwidth channel between origins.

Martin: Important to remember that attacks only get better over time.

Martin: Mitigations seem OK. I think they only need a handful of buckets.

Tess: They did a developer survey that came up with the conclusion that 4 buckets isn't enough. They seem to want 10.

Martin: I think 10 may be OK based on those stats - though web sites will always want to know as much as possible.

Martin: Dropping some buckets (reduced resolution) below 50% capacity seems reasonable, as you aren't as interested in that zone.

Tess: Do you think 10 would be fine without a permission prompt?

Lea: I would worry this may contribute to permission prompt fatigue.

Martin: Could be OK without permission. If allowing more buckets with an open mic (for example), the number shouldn't be a huge amount more.

Matthew: that case (open mic permissions) is mentioned - but for quite a high extra number of buckets.

Lea: They do state they chose linear bucketed approach.

Martin: They wanted events for when it changes, which I think suggests pure buckets.

Lea: That's a little strange, though, as it depends on the number of buckets. I thought the resoultion of the buckets could change in future if they're not serving needs. Does events make this a problem?

Martin: No. If we ship with 5 buckets, and then go with 10, they'll get events with whatever the value is more often.

Lea: I'm not following.

Martin: If the value that's exposed is rounded, then if the code is "if load is below x, change to a lower/higher resolution thing" then it's fine.

Lea: Developers may make decisions about code they can run on an event depending on how frequently it fires.

Martin: Sure but that'd only change dramatically if you added a _lot_. I think this is probably acceptable in the sense that if you expected a low rate of events, but got a higher one, some adaptation may be needed, but I don't expect it will change that much (in which case some signal processing would be needed).

Lea: Does "update" make sense as an event name? I guess it's on render capacity.

Martin: It's OK.

Lea: I think "change" might be more compatible with other event names.

Matthew: How similar do we think this should be to Compute Pressure API? Same interface, different buckets OK?

Martin: Compute Pressure is about general compute resources, this one is more about the ability of an Audio thread to maintain performance.

Matthew: This seems consistent with the past discussion on this topic - sounds like we're OK with what they have.

Martin: Yes, this seems fine - though I would push for a lower number of buckets than what they have, as it can always be changed.

Lea: In that case we could suggest non-linear buckets.

Matthew: That's different to Compute Pressure (but OK if justified, as it seems, and documented).

Martin: Compute Pressure is labelled (nominal, fair, etc...), so different already.

Peter: Don't see a problem with non-linear, which might reduce entropy for some people.  That might be better for privacy.

Lea: Beyond bucket sizes/boundaries, what's the DX? Starting/stopping listening. If you have code that draws the graph... where does this fit in? Continuous monitoring, or only some of the time?

Martin: I imagine with an event-based model, you listen and receive the event. Switch level based on threshold.

Lea: When do you decide to listen?

Martin: Always.

Lea: If you listen to it always, why do you have to opt in?

Martin: So the browser knows where the event to be delivered.

Lea: In that case, could the event be on the AudioContext? It seems that starting and stopping is adding friction. If it was performance intensive to listen to it, that's one thing, but if you listen consistently, this is boilerplate.

Peter: [ scribe missed this; sorry! ]

Lea: I thought this is basically throttling.

Martin: I understand this is a window over which it's averaged ("over a period of half a second, tell me what the load was") - in which case having start and stop makes sense.

Lea: There could be a property that sets the granularity.

Lea: Meta point: this is why we have labels in the new process for these things - we need to ensure that API design issues (for example) are covered, as well as security and privacy (etc.)

Matthew: How to handle >100% with buckets?

Martin: There was a counter proposed (which presents a possible side channel) but if you just report "over 100%" then you're in a pretty good position.

Matthew: There was discussion that the capacity can be computed now (with timers) - should we be concerned about that?

Peter: It's not clear why they went with the event-based approach over polling, from the explainer doc.

Peter: event name "change" works for events fired when it _changes_ but if it's on an interval, then "update" is more apt.

Martin: +1 (as above)

Lea: We should have a principle on this (interval vs changes)

Peter: +1

Peter: Also on this one I think it shoudl be a change event (only fired when it changes). When you start observing, you could say how much of a change you want to trigger a firing of the event.

<blockquote>
  Hello there! We looked at this today during a breakout. 

Other TAG members will comment on other parts of the proposal, but we had some questions wrt API design. We need to better understand how this API fits in to the general use cases where it will be used. Currently, the explainer includes a snippet of code showing this in isolation, where it is modifying parameters in the abstract. What is the scope of starting and stopping this kind of monitoring for the use cases listed? Are authors expected to listen continiously or sample short periods of time (because monitoring is expensive)?
  
  If they are expected to listen continuously, then are `start()` and `stop()` methods required? If the only purpose of these is to set the update interval, that could be a property directly on `AudioContext` (in which case the event would be on `AudioContext` as well and would be named in a more specific way, e.g. `rendercapacitychange`).
  
  We were also unsure what the update interval *does* exactly. Does it essentially throttle the event so you can never get more than one event per that period? Does it set the period over which the load is aggregated? Both? Can you get multiple `update` events without the load actually changing?
  
  Lastly, as a very minor point, `change` is a far more widespread naming convention for events compared to `update`, see https://cdpn.io/pen/debug/dyvGYoV `update` makes more sense if the event fires every `updateInterval` regardless of whether there was a change, but it produces better DX to only fire the event when the value has actually changed so that every invocation is meaningful.
</blockquote>

<blockquote>
We think that the general approach to managing side-channel risk is acceptable.
  
Overall, fewer buckets would be preferable; at most 10, though preferably 5.  Though surveys indicate that some number of sites would be unhappy with fewer than 10 buckets, there is an opportunity to revise the number of buckets over time based on feedback on use.  Increasing the number of buckets should be feasible without affecting site compatibility.  Starting with a more private default is the conservative option.  Increasing resolution carries a small risk in that change events are more likely to occur more often (see API design feedback).
  
More detail is ultimately necessary to understand the design:

1. Is hysteresis involved?
2. Is the reported value a maximum/average/percentile?
3. What happens when the load exceeds 100%?
</blockquote>

### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

Matthew: Seems similar to the above - though more focused on playback, and using an interface established in RTC.

Lea: Let's ask on both reviews for a comparison between the two proposals?

Matthew: +1

*Also general agreement*

Peter: [ scribe missed this; sorry again! This was I think about contrasting polling vs event approaches ]

Peter: Whom should post what?

*NOTE: Editing comments in above issue's entry.*

Tess: Martin for privacy part. Should be clearer about saying that 10 is too many, and we can increase it later if need be.

Martin: I think 5 would be fine. Though it won't be enough for some people, it's a good place to start.

Peter: If non-linear would it be easy to deal with fewer buckets?

Martin: I think once you're down as low as 5 you're probably fine. You want to know if you can adapt up, or down. Could argue for higher res at both ends.

Peter: Could get a value that tells you how much you need to move to get to the next bucket.

Martin: *drops non-linear comment*

Martin: Not keen on changing number of buckets if mic is open.

Tess: +1

Lea: I posted on #843 and asked about the differences between that and this one. Foreshadowed more comments to come on #843.

Peter: Anyone want to post similar on #939?

Martin: I would go further and ask for stronger justification for #939.

Martin: *about to post on #939*

### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

*(We didn't get to this one; oops!)*

## Breakout D: Special session on TAG Appointments

Present: Dan, Tess, Peter, Ralph, PLH, Wendy, Martin, Matthew, Yves, Tantek, Tzviya, Elika, Chris Wilson, Coralie

Regrets:

### Discussion on current state of the TAG appointees

## Breakout E

### [Gamepad Trigger - maybe close](https://github.com/w3ctag/design-reviews/issues/933)

*bumped to next week*

### TAG Appointments
