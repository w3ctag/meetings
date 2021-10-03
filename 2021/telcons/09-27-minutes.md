# TAG Teleconference
#### 27-29 September 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-09-27](https://www.timeanddate.com/worldclock/converter.html?iso=20210927T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
* [Private Network Access (aka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @ylafon, @hadleybeeman, @plinss
* [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov
* [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov
* [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) - @torgo, @rhiaro, @atanassov
* [Pre-CR review of CSS Cascading and Inheritance Level 5](https://github.com/w3ctag/design-reviews/issues/678)

### Breakout B (US / APAC) - [2021-09-28](https://www.timeanddate.com/worldclock/converter.html?iso=20210928T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* n/a

### Breakout C (APAC / Europe) - [2021-09-28](https://www.timeanddate.com/worldclock/converter.html?iso=20210928T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo
* [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @kenchris
* [Conditional Focus (Wehn Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679)
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

### Plenary Session - [2021-09-29](https://www.timeanddate.com/worldclock/converter.html?iso=20210929T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)


* Breakout Rollup
* Issue Triage


-----


## Breakout A

Present: Dan, Peter, Yves, Kenneth, Rossen, Hadley, Amy

Regrets: Lea, Tess


### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman

Dan: I had a conversation with Kaustubha, asked her to comment on the TAG issue with the stuff they've done to help us concentrate our effort on what we should review.

Amy: no response on my issue

Dan: I've emailed the requestor ...

[bumped]

### [Private Network Access (aka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @ylafon, @hadleybeeman, @plinss

Yves: I need to reply - they didn't understand what I meant on diffeence between local network and privsate network - devices physically on your local network. I will reply on that.

Peter: agree they didn't seem to understand...

### [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov

Dan: stil blocked on first party sets...

### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov

Ken: looks pretty sensible - sending other data along with your distributed tracing... along with tracing you can send your own custom data.. metadata... 

Hadley: what kind of tracing?

Ken: open telemetry project... open telemetry uses it...

Dan: isn't metadata sometimes problematic?

Ken: custom data - tracking your own thing - e.g. i'm running on azure ... could be potential privacy issue...  There's a lot of telemetry people who use orchestration.. kubernetes... based on w3c distributed tracing spec... microsoft thing dapr.. https://docs.dapr.io/developing-applications/building-blocks/observability/tracing-overview/ https://opentelemetry.io/

Hadley: use cases doc?

Rossen: question around motivation.. mostly driven by this is a thing people are doing it can we standardise it please. I'm not opposed in general. But without the clear use case it's hard to piece together why this needs to be standardised, which pieces of it make sense, and the overall...

Ken: They already standardized dist tracing - this is an extension...  

https://docs.dapr.io/developing-applications/building-blocks/observability/tracing-overview/

https://opentelemetry.io/

Rossen: trace contexts spec? Is a recommentation... 

https://www.w3.org/TR/trace-context/

https://www.w3.org/groups/wg/distributed-tracing

Dan: but it's adding a side channel for custom metadata - so absolutely agree with hadley show me the use cases...

Hadley: i'd feel better if we can bottom out what the mitigations are...

Rossen: how did this go to rec without going through tag?  In Feb 2020?

Ken: I feel i've seen this - in tag review...

[looking for any TAG review we may have done and not finding it]

Hadley: I"ll leave a comment



### [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) - @torgo, @rhiaro, @atanassov

Amy: there's been no response to dan's comment...

Dan: I went back to the original speculation rules review (#611) and [asked](https://github.com/w3ctag/design-reviews/issues/611#issuecomment-923754268) about the process issue. Too early to build on top. We shouldn't be progressing this review.

Amy: close too early?

Dan: prefer pending external feedback, also asked about multistakeholder

Peter: closed as too early. If it hasn't met the threshold as being included in wicg why are we spending time.

Dan: it's worse - the thing it's built on top of isn't in wicg. I don't know what the temperature check of the developer community.. what implementers generally are thinking about speculation rules.. but we can close as too early

Peter: I'd like to hear the answers to the questions, but it's way before.. Getting input from wicg is first step before you come to the TAG

Dan: [leaves closing comment]

### [Pre-CR review of CSS Cascading and Inheritance Level 5](https://github.com/w3ctag/design-reviews/issues/678)

Rossen: css cascade level 5 is so hot right now. Hottest thing since CSS cascade level 4.

Dan: talked about it in plenary last week but nobody was around to own it

Amy: [puts hand up]

Rossen: focusing on the additions --- new things added - one of the higest level things was cascade layers.  In my opinion probably the most dramatic change to css cascade for some time... 

Peter: I think it's the only significant change between 4 and 5...

Rossen: also a big change in capability to developers - you want to be able to have groups of style sheets - e.g. from different teams in your org - and you want to be able to define who overrides whom.. being able to create islands of content styled correctly... layering sets of stylesheets - for any part of your application.  

Ken: implementations?

Rossen: furthest is mozilla... chromium is also implementing...  It's HOT!


[discussion of web 3.0. Which isn't a thing.]

## Breakout B

Present:

Regrets: Lea


Canceled


## Breakout C

Present: Dan, Amy, Ken, Yves, Hadley, Sangwhan

Regrets: Lea


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo

Dan: recent comment about mapping to w3c specs, I don't understand

Sangwhan: [responds] I think it's a misunderstanding. No comments about other parts. Also see their [issue 15](https://github.com/w3c/miniapp/issues/15)

Dan: needs to be more docs about web page / web app lifecycle and that this work needs to happen in that context.

Sangwhan: message should be - yes miniapp lifecycle is important, but it's implicitly also a page lifecycle. We don't want two separate specs saying different things in different formats, we want consolidated spec 

Dan: I can see the need for if there are additional things in miniapps it should be pointing to a accurate page lifecycle spec and saying in addition miniapps register this kind of service worker or are using these other kinds of technologies, these are the additional steps in a miniapp lifecycle. But it should be using a page life cycle as a core. But the problem is there is no accurate maintained page lifecycle spec.

Sangwhan: and because that work has been abandoned it would be great if they could pick it up. Doesn't make sense to have a miniapp lifecycle which doesn't have a page lifecycle defined in it.

Dan: that would be great

Sangwhan: maybe they should know they can supercede an abandoned WICG spec... Page Lifecycle has not be touched for the last 3 years... 

Yves: the best way would be for me to discuss directly with them. If the TAG feedback is it is important that the work on the page lifecycle is continuing, then it should be enough, the WG can drive the work in that area

Ken: lots of history already to that

Sangwhan:
```
I think you can either 1) take on Page Lifecycle or 2) absorb Page Lifecycle into a singular lifecycle spec, and officially deprecate it. Ideally, we think work should happen on both specs - we'll follow up on this.
```

Dan: TAG can host a special call with miniapps and PWA community? Be great to have one place where we talk about lifecycles.

Sangwhan: I think the people working on page lifecycle have moved on to other things

Dan: maybe just needs a bit of energy. Miniapps could be a way to help channel that.

### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @kenchris

Dan: long comment back from requester

Ken: [reads] .. they're asking [something].. I'm going to ask dominic. Feedback seems positive.

Dan: there's a PR.. happening in webapps but the explainer is still in a google doc, I'll ask them to bring the explainer over.

Ken: will add Anne

Dan: if we get feedback by tomorrow we could close at plenary. Other reason to keep it open?

Ken: wait and see. Want to see if Anne and Dominic think their comments.. maybe easy to close, let's wait.

### [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679)

Amy: it's in a private repo

Dan: if this is part of webrtc why isn't it going on in webrtc wg

Amy: It's [in WICG](https://github.com/wicg/conditional-focus/) now. And [discussion in webrtc](https://github.com/w3c/mediacapture-screen-share/issues/190) - long and active, looks like detailed technical discussion. Odd they're asking for TAG review if they're still working out details?

Dan:
```
Hi @eladalon1983 - Looking at the [thread in WebRTC](https://github.com/w3c/mediacapture-screen-share/issues/190), it looks like this is still under active discussion. If so, it seems like it might be premature for the TAG to be reviewing this?  Is the plan to incubate this in WICG and then bring it to WebRTC for a future WebRTC rechartering?
```

Amy: short security/privacy stuff.. can dig in and see if there's anything else we should flag on that.

Dan: I'll assign us

Sangwhan: mismatch between different browser vendors on how many people work on webrtc, causes interop issues

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

Sangwhan: do we have a compute pressure api equivalent for gpus?

Ken: no they don't have that telemetry yet

Sangwhan: risk that a web gpu kernal could choke the gpu to a point where [???]. A WG being chartered

Dan: from process and multi stakeholder perspective this looks good

Sangwhan: disagreement about what to use as shading language seems to have been resolved. SPIR-V and HLSL

Ken: ended up doing their own. Now there's WSL or something. I hope this new one is more webby.

Dan: concerned about fingerprinting and any kind of cross processor vulnerabilities

Sangwhan: a few ways to leak information through webgl, and webgl is a massive fingerprinting surface. This probably opens up more holes. Should this be permission gated? It's incredibly powerful. The memory model part is a concern for me. The fact that gpu memory protection is a bit less .. not as battle tested as cpu memory. Hasn't been abused as much. There are plenty of cases where crappy gpu driver can leak information through the vram

Dan: let's ask these questions

Sangwhan: nothing they can do about it if the gpu driver is bad. In that case should we even do this work, but there's a huge user need / industry need.

Dan: we should be encouraging them to document risks and come up with mitigations

Sangwhan: I think they have a section on this

Dan: S&P review is not talking about fingerprinting at all.

Sangwhan: [they do](https://gpuweb.github.io/gpuweb/#security-privacy). Also DoS. Thing about [memory security](https://gpuweb.github.io/gpuweb/#security-rowhammer).

Dan: don't have specific mitigations

Sangwhan: sort of impossible becausae browser level implementers don't have control over memory controller

Dan: yes and one can find oneself on a webpage that invokes this api by following a malicious link, so it's much easier to get into this situation when you are on the web so just saying it's no different than a native app - people usually make an affirmative choice to install an app, but you don't necessarily have that choice when you're talking about the web, hence safe to brows, blah blah blah. We need to put pressure about mitigations and potentially a permissions step

Sangwhan: permissions definitely something I'd bring up. Mitigations are tricky - drivers are controlled by AMD, nvidia, Intel, ...

Hadley: worth talking to them? Might be the way the industry is going, not just the web.

Sangwhan:  a lot of work has been done on the CPU. I'll try to leave feedback. It's tricky. GPU driver stuff is completely proprietary. Different drivers/gpus have different issues. Complexity of the problem increases. I'll draft a comment.

Dan: I might paste in the safe to browse design principle and reinforce this point.

## Plenary Session

Present: Kenneth, Dan, Amy, Sangwhan, Peter, Yves, Rossen

Regrets: Lea, Hadley

### Breakout Rollup

#### Breakout A

Dan: FPS and Same-Party cookie, blocked waiting for feedback. Private network access - Yves left comments and requestor responded looking for clarification.

Yves: I'll continue

Dan: Distributed tracing baggage - potential privacy issue, hadley left feedback.

Ken: don't think we reviewed distributed tracing api either

Dan: closed prerendereing speculation rules as too early. Speculation rules itself is early.

#### Breakout C

Dan: miniapp lifecycle and how it needs to relate to page lifecycle, left feedback. Yves also going to progress that, encourage one effort on these. [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662)...

Sangwhan: what's the browser vendor buyin?

Dan: says no information. Be good to get a read on that. We do have [something from Anne](https://github.com/w3ctag/design-reviews/issues/662#issuecomment-929284686) - responding to Ken's request.

Sangwhan: what were our questions?

Ken: we had two ways of getting the events delivery and you don't want to mix the two, wondering whether you should configure it or not. He didn't really answer that.

Sangwhan: there should be only one active delivery pipeline?

Ken: either you want the raw events, give me all and I'll handle it, or you want these coalesced events. Maybe you can configure it somehow? Instead of having two events, kind of showing side effects - shouldn't do that with event listeners

Sangwhan: when is coalesced events used?

Ken: they have raw events and regular events instead of doing the calling. And they want to have the delivery be different for the two. In reality either you want one or the other as a developer. Either you can handle all these and make sure the js is super fast, or  you want the coalesced events because its a safe choice. Should be default? We suggested there should be a way to configure how you want them delivered. Could be an option to the event listener?

Sangwhan: I'm asking because if you've looked at the hit messages for gamepads, it generates 1000 events...

Ken: right, some can handle a lot of events, most developers can't

Sangwhan: won't it clog up the browser event pipeline?

Ken: I believe they tried to implement it

Sangwhan: too much noise..

Ken: implementation detail

Sangwhan: makes sense because current polling model is bad

Dan: did you see Anne's response?

Ken: not addressing the issue. [writes comment]

Dan: we had conditional focus.. a webrtc thing where maybe it shouldn't be in wicg, asked why is it in wicg? webgpu and wgsl - it's complicated.

Sangwhan: some stuff to report. Chat with [someone] for webgpu in chrome. Brought up concern of power of this api. You could choke the gpu and crash every other tab. Counterargument was that's already possible with webgl. Should we revisit this where webgl is permission gated? Would that break too many things?

Dan: any time we get an argument back about a safety issue that you can already do it with this other thing, that's becoming a dark pattern to our work

Sangwhan: enough of one that we should think about setting an example, decide to revisit and permission gate things

Dan: and maybe a design principle that it is not adequate justification for having a damaging property of your technology that you can already do it using some other technology. That simply broadens the surface area of attack. It's not okay to say you can already do it using this other thing. Very handwavey too. New APIs add more possibility for damaging behaviour. Very frustrating.

Sangwhan: whenever somebody detects a problem in the current platform and they're using that as a reference to build new tech on I have this feeling we should be more proactive about trying to address these problems that were introduced to the web, hopefully without breaking it. WebGL is a huge fingerprinting surface. WebGPU is trying to address it by reducing the finterprinting surface, but even if webgpu improves this, webgl still exposes it. So what should we do?

Dan: we should put more pressure on them to document the abuse scenarios. 

Sangwhan: they have extensive abuse section

Dan: so what are they doing about them?

Sangwhan: nothing at the moment

Dan: everything should have a proposed mitigation. Mitigation in a general sense. What are the normative requirements on the.. I'm not sure that permission gating is the answer either

Sangwhan: not convinced it's ideal, just a tool we have

Dan: maybe there are other tools. Concept of if you want to exploit this particular high power api then these other things get taken away from you. That kind of quid quo pro kind of thing.

Sangwhan: doesn't make sense to ask for webgpu to be gated but webgl stays the same. Not consistent. But I'm sure saying starting from tomorrow all webgpl has to be permissioned a lot of stuff will break

Dan: what about some requirement for sustained engagement or.. these are things the user agent can do. In the same way the UA might not allow a webpage to request notification permission when you've never been to that site before. It could also require meaningful engagement with the web page before enabling access to webgpu or webgl. Something more like user activation ++ where it can't just be you moused over a page or activated a control, got to be something more ..

Sangwhan: I thought about that, not sure if it'll work. When you have a unity web game the user won't be actively interacting with the page becasuse the engine is initialisng in the background but has to have access to start up and set everything.  Doubt the user will engage with a loading screen.

Dan: What do operating systems do to protect users from these kinds of attacks? They require code signing. Out of the box it's difficult for me to download and install an arbitrary application on my mac, it forces me to go through a step where I have to say yes I accept that this is from an external developer, not recognised code sign etc. Is that something we need for these kinds of powerful applications? To enable people to do cool stuff? Maybe we do?

Sangwhan: definitely worth looking into. We are getting more and more powerful apis.

Peter: +1 general sentiment

Dan: not clear what the mitigation step is. More pressure on them to think of the mitigation. Not up to us, but they have to come back with some kind of strategy about the risks

Sangwhan: webgpu there's a clean mitigation .. when you initialise webgpu you ask for a device. Currently that's a promise. That can be gated behind a permission. When a script asks for a device a permission dialog pops up and says this application wants to use your gpu (this can mean many things etc..). The counter argument to the permission dialog is basically average users press yes to everything.

Dan: especially a game.. something you want to play the game.

Ken: I want to play candy crush NOW

Sangwhan: .. if a certain blog post asks for a permission.. regardless of it being nonsensical average user will still press yes.

Dan: possibly. Or they won't think, I want this out of the way to read the blog post. That's how people think about cookie warnings.

Sangwhan: numerous dark patterns that will emerge if we introduce a permission dialoge... 'please press yes to the permission dialog'.. it's already happening. Not a real long term solution. User activation doesn't work for this use case, so i'm stumped.

Peter: I don't think it's on us to design the mitigation. Need to put pressure on them. No one size fits all. We can't say everyone throw behind a permission or user activation, going to be different based on what it is.

Sangwhan: apparently a chrome-specific feature that can be used for this. It's nonstandard. Not an ideal path forward.

Peter: used for the mitigation?

Sangwhan: in one implementation, not helpful for standard. [Something used for detecting 'bad ads'](https://www.forbes.com/sites/leemathews/2020/09/09/google-chrome-block-bad-ads/) I think..

Ken: if it uses too much cpu and stuff

Dan: like a profiling what's actually going on? 

Sangwhan: heuristic based, rulesets. Permissions is probably easiest way forward but not a very good one.. better than nothing. Where should we file this?

Dan: I opened up a [design principle issue](https://github.com/w3ctag/design-principles/issues/340)

Sangwhan: I want to track permissions, user activation, what do we recommend when that doesn't work? and what do we recommend when that doesn't work?

Dan: feels like design principle or something on the agenda for the privacy tf. Something more design principly, not specific to privacy, also about DoS and other abuse.

Sangwhan: and about usability.. do you want 15 permission dialogs..

Dan: yeah

Sangwhan: I think the answer is no

Dan: a new design principles issue on that?

### Issue Triage
