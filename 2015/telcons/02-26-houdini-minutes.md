# TAG Teleconference 
2015-02-26 (Houdini, etc...)

## [Agenda](https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/02-26-houdini.md):

* [Mailing List Code of Conduct](https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/02-26-houdini-minutes.md#mailing-list-code-of-conduct)
* [CSS Extensibility / Houdini TF](https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/02-26-houdini-minutes.md#css-extensibilityhoudini)
* [Meetings & Events](https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/02-26-houdini-minutes.md#meetingsmeetups)
* [WebRTC privacy issues?](https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/02-26-houdini-minutes.md#webrtc-privacy-issues)
* [Progressing Domenic's draft on promoting Polyfils](https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/02-26-houdini-minutes.md#draft-on-promoting-polyfills)

Attending:
* Dan Appelquist (dka)
* Peter Linss (plinss)
* Tim Berners-lee (timbl)
* Mark Nottingham (mnot)
* Alex Russell (slightlylate)
* Travis Leithead (travis)

## Mailing List Code of Conduct
See [draft document](https://github.com/w3ctag/w3ctag.github.io/blob/conducttweak/about/tagmlcode.md)

dka: one of the things we're discussing is the mailing list thing.... I was calling it a code-of-conduct...but call it what you will, it's a mailing list FAQ or best-practice document.  

dka: mnot and I have been collaborating on it. If people are happy with it, suggest we make a resolution on it + publish.  

dka: how do people feel about that?  

mnot: I got some input privately that it's surprising that TAG members aren't under an obligation to read all the messages on the list  

mnot: I pointed out that if the list is more functional and focused, we can drop it. If it's a manageable list that's focused, that's something different  

dka: this is aimed squarely at an issued rasied by many poeple  

dka: I see it as a win that there's vigorous discussion  

dka: some criticism from some TAG members has taken me by surprise. Even if it's a bit tangential, its perhaps good that it's vigorious  

dka: that statement is aimed at keeping this from ratholing  

timbl: which statement?  

dka: the code of conduct mention of list readership  

dka: the specific issue is the note that TAG members aren't bound to respond  

dka: the note is that if something is tagential to TAG work, we aren't obligated to get into the debates  

timbl: it's good for people to be able to hash out hairy points  

timbl: in the case of the https thing, going out to the webappsec group was appropriate. It'd be nice to be able to drop in a note that points to that location instead  

dka: I think that's captured  

Alex: I'd like to see quite a few more links in this document. One of the best things we could do is point people to appropriate ways. E.g. put work mode at top and code of conduct at bottom. [be more positive] I'm hoping for a preamble about how we work, how we engage and then a note about the mailinglist.  

mnot: I can get on board with that  

dka: I can see that; leading with a more positive side of it would be good. Also having links would be good.  

slightlyoff: thanks for putting this together. It's overdue.  

mnot: so you think this should pretty different? a workmode doc not a CoC?  

dka: the second part about the mailing list is important, but perhaps the stuff in the last paragraph could move to the top?  

dka: happy to take an action to reformulate  

mnot: happy to help with that  

travis: when would we point people to this doc? When would people read it?  

timbl: there's a pointer from the archives that we can link to  

travis: wondering if we don't want people to see this? If so, where does it go?  

dka: probably on the homepage, underneath the links to the ML  

  

  

## CSS Extensibility/Houdini  

  

dka: Peter, you agreed to give an update, but apologies if this was covered last week  

plinss: nothing different from last week, but we didn't have many people.  

plinss: houdini TF was as few weeks back in SYD. Many browser vendors tehre, very positive, much less contentious than expected.  

plinss: agreement to work on 8 new specs!  

plinss: draft repo here: http://drafts.css-houdini.org/  

plinss: we're going to start defining a box tree; it'll be a read-only snapshot (snippets with limited ancestry). Has traction and APIs being fleshed out  

plinss: other apis include Layout Workers and Custom Painters; opening up the CSS Parser and improving APIs for CSS properties and values  

plinss: work on scroll hooking/customization. Also exposing font metrics. Relationship and timing between style resolution/painting/effects.  

plinss: not much work on specific specs yet, aside from Box Tree. Some terminology to work out.  

plinss: agreement to 2x/yr f2f's and teleconferences as needed  

plinss: wiki page w/ agenda and minutes: https://wiki.css-houdini.org/planning/sydney-2015  

plinss: also, trip reports/tweets coming out:  http://www.mail-archive.com/dev-servo@lists.mozilla.org/msg01131.html  

travis: what was the most exciting thing?  

plinss: that nobody was arguing. We've wanted a lot of this since the 90's and now is the first time when someone hasn't said "no" or "it can't be done".  

plinss: opening up the black box without anyone saying "no" is huge  

travis: this reminds me of Web Components; opening up some elements of HTML  

travis: it makes me fear that Web Components won't get done (due to potential overlap)  

slightlyoff: I'm hopeful we can open up the whole system soon  

travis: I don't have it as a personal goal to open up the whole system divorced from providing value. Perhaps everyone shares that already?  

plinss: none of this was academic. It was all driven by use-cases.  

plinss: I agree there's some overlap between WC and box-tree exposure. Some of the WC use-cases are better served by custom boxes, but until we have those APIs we can't. Until then WC is the only way to do it. This'll let them solve it more cleanly over time.  

plinss: hopefully it'll also help reduce pressure on what should/shouldn't be in Web Components  

travis: yeah, hopefully we'll see more of those natural boundaries when this is laid out  

plinss: e.g., pseudo elements are black magic today. How do you do that today? Extra strucutre == extra boxes.  

travis: related: how does SVG play into the picture?  

plinss: yeah, it has bearing. A lot of SVG impls build boxes in the engines. Consensus was to expose SVG structure in box tree.  

dka: other questions? what's the timeline?  

plinss: it's an ongoing thing. My current concern is that we keep up the momentum and hope it doesn't fall off of people's radar  

dka: would it be better to try to set a time goal?  

plinss: some things are gated on JS features, e.g. value types for CSS values  

travis: is this like a component model?  

plinss: it's direct access to the presentation of the docuemtn. It has correspondence to the DOM, but isn't 1:1. Many cases in CSS already create multiple boxes per DOM and there's no access to that today in DOM/CSSOM  

plinss: e.g. inserting lots of cell formatting in tables  

travis: isn't this already available in getComputedStyle?  

slightlyoff: there are cases, like the ones plinss brought up  

travis: I previously looked into the IE CSSOM APIs to rationalize their CSS layout values. Many made sense, but others don't do the right thing  

(e.g., https://msdn.microsoft.com/en-us/library/ie/hh781509(v=vs.85).aspx for an idea--CSS Transforms also make for funny 'boxes')  

slightlyoff: what about :before/:after? What about multicol?  

plinss: what about pagination? These APIs really do lie to you  

travis: with the best intentions!  

/ everyone agrees  

plinss: with regions, flowing from regions into others, we don't have ways of getting information about this sort of system from the DOM APIs today  

travis: yeah, division of a single logical element doesn't exist today. I wonder how we think about rationalising what we expose today vs. new API  

plinss: the idea with houdini is to stop lying  

[discussion about where name came from, credit to bkardell]

dka: bkardell *IS* the unofficial marketing manager for the TAG ;-)  

[marketing jokes]

travis: thank you for the update! When's the next f2f?  

plinss: probably july/august near the CSS WG F2F.  

dka: there's the TAG F2F in europe in July...  

plinss: probably August.  

dka: we need to lock down meeting logistics for Paris/Berlin. Developer outreach evening up in the air.  

  

## meetings/meetups  

  

mnot: if we're going to be meeting in Berlin, there's a good security community we can engage with. I'd also like for us to talk about developer meetup structure more/less "extensible web"?  

dka: our evening meetups have focused on what we're working on  

dka: just because it's called the Extensible Web Summit doesn't mean it can't focus on other new web technologies/standards.  

dka: I think developer meetups should stem from TAG agenda in order to influence it  

mnot: perhaps I just found the Extensible Web Summit confusing  

dka: catchy name?  

(? Web Architecture Review [WAR] :-) will defer to bkardell...  

timbl: would be good to find another word...houdini and points west? Houdini in a barrel?  

Next f2f: 21-23 in San Francisco, hosted by Yahoo!; - the "summit" on April 20th, hosted by FluentConf  

dka: I've reached out to some folks for lightning talks; if folks have ideas for speakers, plese forward them to me. The idea of the lightning talks is to frame the day. Main event is BarCamp style.  

dka: Fluent has made it free to attend. Will open up eventbright invites soon. At that point, would be great if TAG members can help get the word out then.  

dka: getting great developers there is the priority; particularly people who don't frequently participate in standards. Not an official W3C meeting -- of, but not in.  

http://extensiblewebsummit.org  

  

## WebRTC Privacy Issues
See [blog post](http://www.unhappyghost.com/2015/02/webrtc-killing-tor-vpn-ip-masking-privacy.html)  
  

dka: worrying. When I saw it sent around, it was worrying because it was sent to me by a security expert.  

dka: his summary was "OK everybody, turn off WebRTC in your browsers". This is bad.  

dka: considering that we had WebRTC community members as guests, would be good to reach out and find out how we can help  

travis: at a technial elvel, I wonder what they're finding scarry. I know that WG has been very privacy conscious. It's a surprise to me.  

dka: the worry is about potentially exposing IP of the device  

mnot: this is about NAT traversal, which is hard to do w/o exposing *some* IPs. Has to be exposed at least to browser. Had a chat a while back, may have forgotten some of it. Will revisit and summarize  

travis: sounds great  

traivs: I thought all this happend at ICE layer. Didn't know it had API.  

mnot: TURN/STUN might be involved. Will find detail.  

slightlyoff: concerned that we might have missed something here.  

mnot: we should revisit security/privacy reviews  

travis: screen sharing was the top-of-mind privacy/security issue. Not sure where that stands  

mnot: I've also heard about privacy/security aspects of `getUserMedia()`. We might want to investigate.  

dka: is the concern about the whole thing? Or some area?  

mnot: I was surprised to hear that someone thought MORE UX areas should be specified  

travis: I'm sure the current spec stays away from UI requirements  

slightlyoff: is there new information? new ideas? The old data doesn't incline me to suggest spec-ing more  

travis: agree  

mnot: agree too. Perhaps at most we could investiage guidelines "you should consider..."  

dka: we had a presentation from dom@ at some point about this: https://github.com/dontcallmedom/web-permissions-req  

dka: Dom's point was that some of these things take different requests  

slightlyoff: I'm pretty sure we should ask the browsers to get their houses in order before we go specing this.  

## Draft on promoting polyfills
See [related document](https://code.stypi.com/domenic/Polyfills%20are%20Good%20Finding.md)

dka: something bryan brought to my attention  

dka: this an issue where we have a proto-document  

dka: can't discuss today, but if we wnt to, we need to find an owner

ADJOURNED
