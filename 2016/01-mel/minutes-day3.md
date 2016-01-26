ma# Friday

9:00 - 9:15
Schedule next meetings

9:15 - 11:00
Spec reviews

11:15 - 12:00

What role should TAG take in charter development

lunch 12:00 - 13:30

13:30 - 14:30
Accessibliity with Chaals

14:30 - 16:00

Web components update
IETF update, Captive portals
Houdini Update

Policy interest group

Role of TAG in guiding expermental features in browsers?

16:00 - 17:00 

EWS Blog Post
Stuff we haven't fit in anywhere else


===========================================================
Present: alex, plinss, travis, david, mark, yves, hadley
Remotely: andrew
Guest starring (afternoon only): chaals

# Spec Reviews, cont.

## Issue 93: Review Web Annotations Spec: \url{https://github.com/w3ctag/spec-reviews/issues/93}

Mnot: looks like we left it with needing to sync up with this community. 
... I'll move the milestone so that we bring this up in Feb.
... We'll have Dan extend some invites to the telecon.

## Issue 94: Notifications API: \url{https://github.com/w3ctag/spec-reviews/issues/94}
alex: haven't made progress on this yet.
mnot: I'll adjust the milestone.

## Issue 95: Web Background Sync: \url{https://github.com/w3ctag/spec-reviews/issues/95}
Travis: does this wake up the main browser when the background sync occurs?
alex: it's up to implementation. It might be different depending on devices. The spec lays out details assuming that there's not necessarily a tab open.
... it's a way to schedule work roughly between the timeframe of 'sendBeacon' and the next time the user might visit the site. Like a auto-retry system.
... q: is there a backoff policy? Not sure... 
... Hopes is that when network interface/topology changes, it might be an opportunity to wake up and re-try the background sync.
... Also a provision in the spec for "this is a final attempt", which allows the code to act appropriately.
hadley: given privacy concerns, it makes sense to run this through the W3C process. Does it make sense to have webappsec look at it?
alex: The spec is in a community group right now, not sure what WG it may end up in (they can shop-around, but may end-up in web platform WG).
alex: The API leaves the permission model roughly out of scope. (In many platforms having access to the app implies the ability to do background work.)
mnot: this makes me uncomforatble, seems inadaquate to leave it up to only timing.
alex: true for tabs in background, ect.
... except this has no front-end website to communicate to.
... I think the spec is wise to leave that [details of when to schedule] out of scope.
mnot: folks can get upset when something starts to chew up a lot of bandwith.
alex: like with push notifications in chrome, you can sometimes fail to get information from the server. (browser is killed, can't reach the server, etc.) you don't get to the point to show the notification. We put a constraint on pushes so that after some % fail to show UI, Chrome intercepts and shows a proxy notifications just the user knows that background work is happening.
mnot: for the TAG: the press is full of complaints from folks living on remote islands with limited bandwidth, that have bad experiences with big companies that consume a lot of bandwidth.
alex: one of the opportunities is that the system can coalesce them together (to save battery). This is a primary goal of not having tight controls on when these things can wake up.
mnot: out goal in TAG is not to specify, but to help implementers share concerns.
alex: an implementation concerns document?
hadley: I'd like that. We've set user's expectations, over all the years of the Web, that the user agent won't be doing anything with a particular site when there isn't a tab open for that site. This may be an issue with service workers too.
alex: With service workers, they can't do work in the background (they always correlate 1:1 with an active page). So that is just for push notifications and background sync.
hadley: Okay, then the issue is just there for those two. I just want to ensure that the user can be informed--that they have enough information to decide how to manage their bandwidth, how to react to sites they don't trust, etc.
alex: I'd like to distil these concerns down into a document, with an outline of the concerns and the potential mitigations (optimizations). These would not be normative. Perhaps in a sister document.
Travis: places to avoid the dragons when implementing.
plins: Sounds like all these concerns were taken into account in the design, but they were never written down.
mnot: I think many of these things are generalizable, and could help other related specs.
david: I feel like it should be clear that these mitigations are conformant, and there should be some link from the spec to the document in question. Just so implementors don't miss it and think that they're required to do the thing we don't want them to do.
alex: Another thing I'd like to see in the spec is the error conditions. How does the developer communicate that their synchronization failed (in order to get a retry). I assume you have to wait until the promise is rejected? It would be nice to see that called out.
Alex: Earlier in the design process there were two variants. A recurring sync (every day at 5pm, sync my news). The other was a one-shot activity (I'd like to send this email).
... this spec does not do recurring background sync.
hadley: is periodic background sync on hold or being developed elsewhere?
alex: it's on hold (not being developed elsewhere)
plinss: well, you can just schedule a new sync while the old sync is running right?
alex: I think there are limits on that...hmm, yes, you could potentially request a new one. I'd like to see a discussion on that (when should UA's allows this/disallow this? How does the UA keep the user aware of this? What are the timing implications?
plins: Looks like 'fireSyncEvent' algorithm may say something about this...
alex: step 6 of 5.2 looks like there some clause for it. Wondering if you could ping-pong between elements?
mnot: will express our TAG stance on the spec overall (which is positive)

## Issue 97: Review FIDO Spec: \url{https://github.com/w3ctag/spec-reviews/issues/97}
mnot: Will schedule time to review in the near term.

## Issue 98: Push API (data payloads): \url{https://github.com/w3ctag/spec-reviews/issues/98}
david: wanted to look at this in more detail, but haven't had the chance yet...
mnot: FYI: Martin Thompson's proposal for encryption (content encoding) has been adopted by the http group.
plins: purpose of that?
mnot: we can now have content-encoding encrypted, server can still read the meta-data to process it, but the payload can be encrypted.
Yves: does \url{https://tools.ietf.org/html/draft-ietf-httpbis-encryption-encoding-00} relate to \url{http://tools.ietf.org/html/rfc6249} ? (for the replicated content use case)
mnot: here is the actual format spec: \url{https://httpwg.github.io/http-extensions/draft-ietf-httpbis-encryption-encoding.html}
... it's very specific about the encryption algorithm to use. We didn't want to have an open-ended encryption becasue we've seen that go awry.
david: do the keys get setup when registering for push API?
hadley: is there a use-cases document?
mnot: this was mostly setup for Web Push and storage server like DropBox.
hadley: those are pretty specific--would be nice to make this explicit
Travis: How does this play with existing push models like those provided by Apple/Google/Microsoft
Alex: defines how to encode a body. Can be transported over a variety of protocols that allows a 'body' - spec defines how to decode that body.
... see also: \url{https://w3c.github.io/push-api/#sequence-diagram}
mnot: spec was tailored to have minimal impact on HTTP, but the format can be reused elsewhere.
alex: looking for the canonical demo code... looks like: \url{https://tests.peter.sh/push-generator/}
hadley: how is Dec. 31 content encryption draft different from \url{https://tools.ietf.org/html/draft-ietf-webpush-encryption-01}
mnot: general content encoding is for any HTTP. The other is specific to encryption for Web push. It's not for TLS to un-encrypt, but may be able to sit encrypted on a push server until its ready to be decrypted at the end-point.
dbaron: is there any best practice about redoing registration in order to generate new keys at some points in time?

## Issue 99: HTTP 451 Status: \url{https://github.com/w3ctag/spec-reviews/issues/99}
mnot: We discussed in the call. Not sure we have anything more to discuss?
all: nope.
mnot: closed.

## Issue 101: Privacy Mode: \url{https://github.com/w3ctag/spec-reviews/issues/101}
mnot: we just opened this. Placehold to look at in the future.

# Future meetings
mnot: hosting in London!
hadley: looking for building venues with help from Google/Mozilla?
dan: I found a room... well technically, a room was offered to us.
... Would be nice to arrange both a hosted dinner and developer meetup.
mnot: a meet the tag meetup?
dan: yes, I need to find a host for that.
andrew: I could host the meetup?
July meeting: 28,29,30 July meeting in Stockholm, SWEDEN
Thinking of adjusting post-TPAC meeting from Sept. 27-29 to week of Oct. 17 in San Francisco.
Tentative January 2017 thoughts: week of 16th or 23rd? (no location).

# What role should TAG take in charter development

mnot: it'd be nice if the TAG could weigh in on the architectural merit of charters -- and thats about it.#
alex: How would that differ from us getting an early view on the specs?
... We frequently have technical feedback about specs
... We have personal feelings about charters, and we have organiational commitments about them.
mnot: Do you think there isn't anything architectural in charters?
alex: Charters are about spinning up a process. They don't commit anyone to implement anything, nor do they commit us to any specific design (like the design of an API). 
... Imagine a "burn it all down and redo it in C++" working group... we'd have something to say about this.
mnot: I hear that. But as a working group chair, I've found a strong charter to be valuable: allow you to scope the work. Set up conditions for success, or failure.
... Charters are an early opporutnity to make sure that what's going to happen there isn't completely misaligned with the web architecture.
yves: You could see that as an AC rep.  Why the TAG...?
mnot: Sure
alex: You could imagine a pull-based function. The AC could refer a group to us... That wouldn't subvert the AC's rightful membership-driven ability to set the agenda, but also wouldn't put us out of step with what's happening.
...Where AC reps are unhappy about a proposed charter... they could put us in front of it.
mnot: I don't think anyone is suggesting that the TAG be required to review every charter.
alex: I'm positing different modes in which we might be involved.
peter: What would we expect the outcome to be of a TAG reivew? Kill working groups before the start? Changing their scope?
alex: Frankly, it would be nice to do what we did with Payments... "Hey, it sure would be nice if there was a technical document to review by the time we get to a charter."
...Maybe we should say that to the AC and the AB?
travis: That lends itself to not forming a working group until you have a proposal
mnot: One model would be, if we had the opportunity to look at a charter when it's first proposed to the AC.  Then decide where we could get involved.
dka: That's kind of what I was thinking. I don't think we want to put the TAG ito the critical path of charter development.
... But there has been discussion about needing more technical scrutiny about charters as they're developed.
...I was looking at mnot's coments on the payments charter. Some of those were architectural: these deliverables aren't sufficiently scoped.
...That's technical feedback.
...That's the kind of feedback we would have agreed on, in the TAG. Maybe we could've had a bigger, more positive impact if we'd been involved earlier. 
...But I don't think we should be in the critical path.
mnot: Yes, I don't want to increase our workload significantly.
dka: Would it make sense to replicate our spec review process with charters?
...I.e., if the team or whoever is developing the charter wants feedback from us, then they can register it in our Spec Review repo and we can add it to our agenda.
mnot: We have people putting IETF specs in our repo, so it may fit#
alex:  I'm biased towards wanting us to setting expectations with people who come to us for advice, so we can provide meaningful assistance.
...At a basic level, we can provide better guidance to them if they came to us with a technical document.
...If we could put up a sign that says "your charter should include a technical document".
...If the AC and AB want us involved in charter review
mnot: We're in this state where charters don't always.  
...We can either address that as the earliest opportunity to give technical feedback. Or we can tell them not  to do that.
hadley: in semantic work in w3c, we sometimes start with something already written elsewhere (with adoption), in which case process Alex describing makes sense.  Sometimes, re things like best practices, trying to codify things commonly done but not written up.  WG process starts with writing it down and getting agreement.  Want to have that work done somewhere, and W3C a good place.  Not yet convinced WGs the only place for that, but hesitant to say all WGs should start with something already being done and just validate them.
hadley: Second, wonder if role for TAG in starting new WGs; sparking new charters to happen.  Part of architecture of Web is looking at where the holes are and highlighting them as holes.
plinss: We have in the past informally said a WG should exist.
mnot: I think ... I see where Alex is coming from. It's probaby workable. For the more browser-touching parts of the W3C, there is a strong incentive to have a spec. This provides a natural way to get TAG review in a timely fashion.
...I'd be worried if there was some implication that the TAG should sign off on every charter.
Hadley: I don't disagree with that.  We shouldn't need to sign off on every charter.
david: We could ask to see these docs early, maybe around or before when they move from a community group to a working group.
alex: We are seeing that already -- look at Background Sync.
...Some of these things are at the level of polish that you would expect something that's already on the standards track.
hadley: to our chairs... how resolved to we need this discussion to be?
peter: ¯\\_(ツ)\_/¯
alex: Where MIke has expressed enthusiasm, we may want to express we are concerned about being a fixed part of the process, but we could say we prefer to see technical documentation and designs.
mnot: We review specs.
alex: ..for designs.
mnot: so charters with weak technical documentation can expect feedback from us accordingly.

hadley: Do we need to do anything with these conclusions?
dka: ¯\\_(ツ)\_/¯ I don't think so.


# EME and the proposed non-sue covenant... 

Yves gave an update on that and the proposed extension to the HTML Media Extensions group

peter: The AB have reached out, asking for more context from us following TPAC.
Hadley: I think we commented on the architectural parts of this.
dka: The TAG doesn't have an opinion on this particular covenant.
...The reason we issued the statement is because we think seucrity research is important.
mnot: So they are suggesting a specific implementation... it may be that it isn't the best way to implement it, but it's not our remit.
dka: I feel like we should encourage W3C here to not ignore this issue.  I think this is indeed an issue.
...If we can respond saying "We don't feel it's our remit to address the legal parts of this, but we do feel that action would be good."
...If not, I think the statement from TPAC stands.
alex: agreed. We stand behind that.
mnot: I think individuals can comment, but it's inappropriate to have a representative of the TAG in that conversation.
hadley: I totally agree. I can't see any parts of this beyond what we've already commented on.
travis: There are a lot of personal opinions, lawyers, and other economical and political issues intermixing here. I think the TAG has done our part.
dka: I'll reply to the AB.


======== Lunch =========

<back from lunch>

# Accessibility

Topic: special guest star Chaals
chaals: history of this discussion starts from two previous TAG meetings in Berlin and San Francisco; there's a common thread that runs through them which is about ??? ...and ARIA is like Web Components
alex: not really thought? Web Components has an open vocabulary that you can extend and ARIA doesn't
chaals: ARIA lets you add meaning to elements that otherwise didn't have htem; e.g. people were making buttons out of <divs>.
travis: you need this because you need machine-understandable context?
chaals: you need this even when sighted; i.e. without using a mouse can you navigate search results on yandex.com? The issue isn't that this is broken in ARIA; and ARIA works fine. ARIA only works with a subset of a11y needs, though. Current practice is that Browsers don't need to do things themselves. Browsers live on systems with their own a11y APIs (some good some bad) and ARIA maps that information into those system a11y APIs. It works fine (modulo bugs).
chaals: this works less well for folks who don't have traditional dissabilities; i.e. aren't using a screen reader (which is most people with disabilities). One of the problems is that putting configurability into a browser is considered a bad idea by browsers. For some folks, though, it's considered a necessity.
<discussion of the value of adding options>
chaals: what longdesc was designed to achieve was that there would be a description of a resource that nobody ever hand to look at but which would be there if you went looking.
travis: I recently had to upgrade the UI events spec and the tools dissallowed <summary> and the advice the tools gave was roughly "make your tables more semantic". I looked, saw they were pretty good, and deleted my <summary>ies. That speaks to wanting the things you put in the page to be usable by everyone.
chaals: the idea that you're going to reflect things only to assistive technology is wrong. Some folks get the benefit of what's done for ARIA but most don't, particularly because the browser doesn't bake anything in.
travis: these are not multi-modal input users?
chaals: these are folks who are not constrained by ???
travis: win10 finally updated the lock screen so that I didn't need to use a mouse in the login screen
<discussion of browser handling checkboxes vs aria description of checkboxes>
travis: assisitive technology are inputs to the browser; they're distinct from the browser itself
chaals: yes and no; minimum font size and page zoom are built in. It's the browser doing those things.
travis: but keyboards themselves don't do input, they require humans to interact. a11y tech is unique in that it does this on behalf of users but none of the other input systems can do it over their own volition. They are a middle layer to code in the browser that generates input but they dont' do it themselves.
chaals: sort of. A complex a11y tech can do many things. You can write extensions that handle some of this.
chaals: all of that is very meta and about general principles and it does come down to the, where possible, architecture should support doing a11y as part of what you do anyway. That you should do things once to the extent that you can.
travis: I'm curious to hear your thoughts about incorporating more of what a11y tech does into the browser itself, which I thought you'd alluded to before.
... you're perhaps saying that the browser should take that responsibility onto itself.
chaals: I think there are 2 cases where you want to make the browser more responsible: the first is where the browser itself provides functionality. I.e., things you can customize. The other case is where it'll make a difference to the way developers produce content.
...the argument I brought to berline was the ARIA case, such that if you label something a checkbox in ARIA the browser will handle it as a checkbox vs. asking all developers to get every aspect of the checkbox behavior right.
<discussion of what sense these would then participate>
dbaron: this comes back to why ARIA exists in the first place. When ARIA was being developed, many folks thought this stuff should be in HTML semantics and not be a separate set of semantics. Lots of this has been added to HTML now, but ARIA continues to persist in the notion that it'll only reflect data back to accessibility tools.
chaals: a11y APIs; yes, it has this view that ARIA is not going to touch other aspects.
dbaron: I suspect we're stuck with that. Lots of content would break if ARIA roles/states started to do lots of other stuff than what it does today
chaals: I'm not so sure; ARIA does a limited set of things: to allow you to get widgets, allow them to be discoverable, and make them operable. ARIA doesn't let an ARIA checkbox participate in form submission, e.g.
travis: I think dbaron would say that there is code on websites that would be astonished if these items started participating. You'd get 2 checkboxes, e.g.
chaals: not talking about that, talking about interaction behavior.
travis: where you do draw the line?
alex:  so WAPA is starting but I need to apologise for not having done anything here. It continues to seem to me like a good idea to me to break out the behavior of a checkbox and make it available (not necessarily declariatively) as a trait or mixin, and allow you to make it part of your own custom element.  Comes back to question of what are the HTML elements we have today, and how do we explain them? What are the traits/mixins that <checkbox> is made of today? Exposing those traits seems like a good solution becuse it's one that gives developers power to get this in an opt-in way, and reduces total amount of work, which is a goal you share.
chaals: yes; we need to do something here. Having nothing is really painful. ARIA is, as we noted, a closed vocabulary.
travis: web components are starting to open up this can of worms. We can talk now about how to create you, how to destroy you, and how to handle your attributes, but there's a whole not more to do.
chaals: the "how do you interact with things?" question ties into the question of how you make SVG more accessible. They're running into the same things: they could put a lot of things into ARIA and make SVG tools generate ARIA...but give that most SVG tools generate <unmentionable> content today...
travis: given that it's a graphics format, the needs are...what? To say that "this is a line that goes from 100px to 300px"?
chaals: no, it's about content that's laid out graphically. We have web pages that are words in images. We have infographics and flow charts and process diagrams and chemical processes.
travis: they're very hard to explain; they're graphical because that's a great medium to explain their complexity
chaals: there's a line (continuum?). The nice thing about SVG is that you can break things into pieces and explore things bit by bit. If you could navigate around different kinds of scope that'd be nice. That's kinda hard and I'm worried that if the solution is "lets define ARIA attributes for everything that occurs in graphics!", that seems really really specific and sufferes from the ARIA problem of "who's going to get this information anyway?".
... there seem to be lots of things that make SVG relatively explorable and navigable in a bunch of scenarios
... the argument against longdesc was that "you can do all of this in SVG" which was perhaps true in theory but not in practice.
... we've gotten a long way
travis: can you provide an example of how you'd use an SVG to replace longdesc?
chaals: imagine a flow-chart. I.e. the W3C Recommendation Track Process. It's an SVG. It's got descriptions of things you can do. To do a sensible longdesc you'd maybe point to a section of a document or set of links to further explinations.
<discusison of SVG linking and description mechanism>
chaals: An experiment: \url{http://svg-access-w3cg.github.io/use-case-examples/revisedrec2.svg}
...various things are linked
<discussion of the behavior of the example>
chaals: you should be able to explore a complex diagram and focus on areas you care about
travis: so as dbaron was saying, people who opposed ARIA proposed instead more semantic elements? In this case it'd be great to have a more semantic arrow instead of lines.
dbaron: are there design pricinples we should agree on and document?
chaals: there are principles that I think are high-level, and when it comes down to "so we wrote a spec", it's often easy to interpret them in multiple ways.
... that you can't disentangle checkbox submission from behavior is a bug.
<discussion of developer incentives for re-creating form controls in script>
chaals: so when they do this, they break interaction models when users do things they haven't anticipated
travis: in SVG the idea of an arrow is a new sort of thing, whereas an HTML checkbox is a pre-existing thing you'd want to reuse
chaals: in SVG it's a link. In graphics you draw connections graphically so that when they start moving around...??? These are two-way links. There's a way to hack it up with two one-way links.
... ARIA has a "flows-to" which is intendend to offer a multi-headed link; i.e. something could go to A, B, or C. Reviewing how a11y tech actually works in practice is I think important.
... looking at SVG for cases where HTML does things like it already, I'd prefer that we figure out how to retrofit HTML and figure out how to apply it to SVG instead of coming up with two separate approaches.
travis: it occurs to me that somethign UAs could do to better embrace ARIA -- putting aside that it might not be a good direction for a moment -- ARIA flows-to sounds like "the tab index branches here" but theres an archaic linear tab order but in reality it doesn't reflect what authors are trying to say about how they want their content to be navigated. The browser could be informed by the flow-to graph which could impact tab navigation. It brings up lots of questions.
... I've been speaking with Cynthia Shelly recently about exposing neumonics to the web. In some cases when you press a key in windows, you get a hint on the screen about other keys that you can press that can let you take actions. This can let you teach users using a keyboard about how to navigate around. It seemed like a natural fit. Mozilla implemnets accessKey label and it happens to work in both FF and IE. If it could be a reserved thing in the browser chrome about focusing the content...
chaals: that would give you a mechanism whereby you could solve a lot of conflict issues; lots of things have alt-shift activation (e.g.) and you need to disambiguate them
travis: just wanted to share that; it's a big space.
<what are the AIs?>
alex: we should work to get HTML to explain these things
travis: we should pick a small one. I.e. getting HTML to talk about how checkboxes are actually implemented.
chaals: range might be a slightly bigger leap. Looking at the ARIA spec, with the view of how it fits into the rest of the web....???
travis: as a recent struggle is how you translate the web built for the iphone that don't have other input modes; i.e. that have keyboards but not touch...that's a major challenge. Lots of websites the other way that have hover menus but I can't hover on a phone.
<dad jokes>


## Web Components Update

Alex: There have been productive meetings about Shadow DOM (an isolation boundry for style). Conceptually it's an element, sort of like an iframe, in that it doesn't allow anything to be affected below it. 
David: Cascade but not inheritence?
Alex: Yes. Although they're sort of like document fragments internally. 
Alex: This came out of earlier Web Components designs. They've changed a little bit. The nasty question that's come up is about distribution; some elements are terminal, in that when you invoke them, they're a leaf. E.g., an iframe; any markup inside there won't get rendered. Others, e.g. select and option, will get interpreted. The children get "distributed".

Alex: Earlier designs used an element called content. Long story short, the specifics of using CSS selectors was viewed as problematic, so we now use a system called slots. They're almost as powerful, and simpler for implementers, and shouldn't bring perf problems. Chrome and Apple have implemented

Travis: Edge is preparing for an implemention.

Alex: Shadow DOM can be applied to any element. If you apply it to a div, it will change the layout and rendering of that element. Its primary value is encapsulation. It doesn't leak deails into the outer page; you're not fighting a global namespace for CSS, and for DOM traversal, you don't have to skip over non-semantic elements. That's the benefit.

Alex: The template element is a done deal; it's in browsers. No update.

Alex: Google had proposed object.observe; that's been rescinded from TC39, and we're dropping from our implementation.

Alex: Custom Elements are the ability to invent a tag name, but have the parser helps you out with the lifecycle. E.g., knowing when you're attached and detached. Custom elements provide hooks for this. That work is continuing, there is a F2F in SF in two weeks. The contentious bits are...

Alex: 1) whether you can subclass HTML elements (probably not), 

Alex: 2) whether or not the upgrade from an unknown to custom element is sync or async. This has implications on how you register elements.

Alex: There are unanswered questions about how DOM elements work. Microsoft had some good ideas about that in the late 90's. The property/attribute split is still to be addressed.

Alex: Adoption is growing, both polyfills and early implementation. We see millions of Web pages using components every day.

Peter: Back to slots. I've heard about it, are we talking about mutating the DOM?

Alex: It's projection. You don't change the DOM. 

... explanation on whiteboard ... 

chaals:


   * a shadow dom like 
   * <foo-thing>
   *   <stuff>..<stuff>
   *     <keything><slot name="sloth"></...
   *     
   * gives a "light DOM" like
   * <foo-thing><keything/></foo-thing>
Peter: There's always been tension between DOM and presentation, and this is helping, but we still want to be able to tease this apart.

Alex: That's not what people are trying to accomplish. They're not trying to separate semantic from non-semantic; they're at different layers of abstraction. It's not that you want one layer of nesting of Web components; you may have an arbitrary number of layers. Solving it only for one is a bug. 

Peter: I don't want to prevent nesting. Let's not try to throw all of the presentation out of the DOM.

Alex: I'm disagreeing with the notion that this is purely presentational. It's behaviour too.

Peter: When you're trying new semantics, this is the right approach; when you're just trying to change presentation, there are other approaches. I don't want them to diverge unnessessarily from what we do here.

Travis: Yes.

David: The mental model here is much simpler than the regions stuff, because this is another layer. 

Alex: There is a fully flattened tree that gets used for rendering.

Travis: You can traverse it (carefully) using some APIs on the slot element (getDistributedNodes?). 

Alex: We don't have access to those late stages of the rendering pipeline from script. 

David: The fully flattened tree is easier to understand. 

Peter: This slot behaviour sounds lke it should be explained in terms of regions, and we should fix regions to make that work.

Travis: I agree that it is conceptually similar. 

David: Travis mentioned using CSS to change the shadow dom you have. XBL works the same way. We saw that as the #1 design flaw in XBL.

Alex: Hixie and folks at Apple wanted to use behaviours for this. We didn't agree, because you wouldn't be able to tell as a programmer what behaviour would apply if it were done with CSS at resolution time. We came to understand that this is about the "thingness" of your element. 

Travis: It self-describes, it's accessible, etc.

Peter: Agreed. This has always been problematic. 



## IETF update, Captive portals

mnot: IETF is meeting in Buenos Aires in March, in Berlin in July, and ...  \url{http://www.ietf.org/meeting/upcoming.html} and \url{https://mailarchive.ietf.org/arch/msg/ietf-announce/VX0rSFv-JvdoAa25OyEY\_RVvhos}
hadley: it meets 3 times a year? The whole IETF?
mnot: yes...it's very different culturally. You should come sometime.
... the Application Area WG is being shut down. It's being combined with the Real Time WG and is being joined as the Applications and Real Time (ART) Area.
<more dad jokes>
mnot: there are 3 area directors for that Area.
hadley: what falls into Applications?
mnot: HTTP, FTP, JSON-stuff, email, etc. It's a very small part of what's done at IETF; most work happens at the lower layers.
mnot: there's a new Captive Portals working group. Warren Kumari and Martin Tompson are leading it. There's a new DHCP option that has been proposed and published as an RFC, but there isn't much adoption.
hadley: how does that help?
mnot: one of the challenges is figuring if there's a captive portal on your network.
mnot: Constrained Restful Environments ("CORE") is a new non-HTTP protocol for restful APIs in IoT devices.
mnot: DBound (domain boundaries) doesn't yet have browser involvement
alex: is this IETF defining the boundaries of the Origin model?
mnot: it's the public suffix list, so for cookies and other uses, so not really
mnot: Dispatch is a WG that determines what to do with ideas: very quick resolutions to "what should we do with this idea"? WG, send to existing WG, needs a new draft, etc. It has 3 chairs: Mary Barnes, Cullen Jennings, and Murray from FB.
mnot: GeoJSON WG
<discussion of GeoJSON history>
alex: when was the IETF GeoJSON WG spun up?
mnot: middle of last year?
alex: and the Spatial Data on the Web WG at W3C?
hadley: Looks like the end of 2014
alex: and are they talking?
hadley: I'll find out
<discussion of OGC>
mnot: in HTTP we've adopted igrigorik's Client Hints draft which provides information about viewport size and pixel ratio so that servers can send appropriate content. We're also doing the Encryption draft we talked about before. And we're doing a Key header which is a finer-grained version of Vary.
... doing Alternative Services (which we discussed previously) and Opportunistic Security. Also the 415 Status Code.
... a few cookie related drafts from mkwst to deal with published vulnerabilities. We're revising the cookie spec but doing it through a process that solicits drafts for specific changes to the spec. Once we have a set of drafts that we think are good we'll incorporate them wholesale.
... the only calls for adoption are "Leave Secure Cookies Alone" and "Cookie Prefixes" which adds prefixes to cookie names to change their behavior in certain circumstances.
... mkwst also has a draft that defines first-party and third-party cookies (which isn't defined anywhere else).
<discusison of history of Cookie stewardship>
mnot: we're still working Client Certificate authentication for HTTP/2. Also talking about TCP advice for HTTP/2.
mnot: there's a draft out that specifies a JSON convention for HTTP headers. The draft maps JSON into and out of Headers. Some WebAppSec drafts are using it.
mnot: there's a JSON Working Group charter that will normatively cite ECMA-404; \url{https://datatracker.ietf.org/wg/jsonbis/charter/}
mnot: this charter was approved in late June
mnot: there's a font type registry being set up by me and Wendy
mnot: also a working group for video codecs: \url{https://datatracker.ietf.org/wg/netvc/charter/}
alex: is this related to \url{http://aomedia.org/} and/or the Mozilla work?
mnot: Cisco has put in drafts related to Thor
mnot: sounds like TLS 1.3 will be done Q1/Q2 this year and certificate transparency is still churning along

## Houdini Update

dbaron: my biggest concern is stuff actually happening...
alex/hadley: that it is or that it isn't?
dbaron: we designed many features at last year's meetings but the specs related to them haven't been fleshed out.
hadley: do we know why?
plinss: some things are moving and some things are moving in google docs and other non-spec forums.
dbaron: there's some feeling that Houdini should meet around every CSS F2F meeting, partially as a forcing function
dbaron: there will be another meeting in 2 weeks
travis: can you cover some of the recently proposed concepts? perhaps "worklets"?
\url{https://drafts.css-houdini.org/worklets/}
dbaron: this is the thing we had 7 different names for. The basic idea is that there are many things that Houdini wants to execute inside a constrained JS environment and we want to allow folks to supply JS but only with a limited set of data that we hand it; only stuff that's appropriate to the layout/paint process.
plinss: you can't get access to DOM/Document/etc.
dbaron: you can get access to engines but not change them
dbaron: anticipating some fun discussions with TC39
alex: would like to see that conversation happen SRTL
<discussion of synchronous nature of worklets>
plinss: you won't be able to make calls for async state, etc. And there might be multiple of them running in parallel but they won't have shared data.
travis: we might brainstorm how to allow parallelism over the DOM
alex: or a way to run code in the pre-parser thread?
plinss: we don't want to hand worklets full Canvases, i.e. don't want to allow readback or a11y, so some factoring there. Need to defend against scraping.
<discussion of Canvas factoring>
dbaron: we want to not have a way to store global state, but constructing new execution environments might be expensive, so looking at hacks that discourage people from putting state on global objects
plinss: yeah, you'd use custom CSS properties that'd be passed into you, but you need to set that up ahead of time
travis: makes a lot of sense
plinss: don't want to constrain future implementations unduly
plinss: there's been some progress on CSS OM improvements?
dbaron: the only drafts that look active are Typed OM, Worklets, Painting API, and ???
alex: it sounds like things are moving... are there prototypes? Are they keeping pace with changes?
dbaron: lots of prototyping, not as much capturing what the prototypes do in specs
plinss: hoping for more to talk about after the next F2F

## Policy interest group

chaals: in progress. The Team is doing the work.

## Role of TAG in guiding experimental features in browsers?

alex: if there's a technical document, we'd love to talk about it.
<agreement>
\url{https://www.w3.org/TR/css-2015/#responsible}
alex: oh, wait, forgot about the CSS text about experimental features. It includes text both about not allowing experiments getting too big as well as using prefixes
dbaron: this is new; tab and fantasai added this, basically it says that experimental features should be shipped with and without a prefix. \url{https://www.w3.org/TR/CSS/#unstable-syntax} or \url{https://drafts.csswg.org/css-2015/#unstable-syntax}
plinss: it says that things that are unstable should not be exposed by default on the web
chaals: it should be painful?
travis: we hopped on the flag configuration bandwagon, and we continue to get requests for specific features for specific sites.#
alex: In Blink, we sent an intent to implement... we're roughly calling "the experimental framework". I've talked with Jacob Rossi about this, and the Blink community has debated at some length.
...The notion: we acknowlege that prefixes don't work because the experimental populations get too large.  
...At the same time, it's not great to ask users to change config flags.
...They don't always change them back
...Those experiments can't close, OR they can't get big enough to give you meaningful feedback.
...So it's hard to get an experiment big enough to give you good feedback, but not so big it gets "burned" into the platform prematurely.
...You can't see which sites are using it, nor which users are benefitting from it.
...So we've proposed you register for a key, tied to an origin, ("example.com would like to register for a key), and then you provide that key in the HTTP header. 
...That key unlocks certain features only for your origin.
...Experiments should last 12-18 weeks max, and will have a total cap on amount of traffic.
...Example.com is pretty small. Google.com is huge -- and if it were to participate, no browser would be able to say no.
...So, experiments autoexpire.  And the API will go away.  Your thing will break, and that's communicated to you ahead of time.
...You had to register up front, so you will be someone we can contact. And if you want to use future experiments, you'll have to answer questions about the last one.  So we get feedback.
...Hope: we'll be able to roll out experiments in a time-limited, population-limited, knowable way -- and then take them back.
travis: Sounds fantastic. Can we a) see that other browsers implement a similar registry?  So that implementors won't need a separate key for each browser?
alex: there will be dials and knobs you can turn to make using new features more or less dramatic. If we don't get enough enthusiasm from devs, we might make it easier.
...But there will be public dashboards about usage, and we'll be able to monitor it all.
...I'm optimistic: if it's too painful, it will push us to coordinate across browsers.  You can imagine, in the long rrun, a single registry for keys across browsers.
...In the short run, we want to see how it works for us.
peter: My concern: I'm a random web dev, and I have a contract for example.com, and I want to use these experimental properties... And then the customer doesn't complete the contract, the key expires, and the same properties are now part of the standard but the behaviour is slightly different... and the site is broken.
alex: That site will have been broken for a good long time before the experimental feature becomes standardised.
...Or process will require changes between the experimental version and the standard.
...Part of signing up to the experimental population is saying you do want to be a part of this, ongoing.
peter: My concern is that devs try to be clever... The experiment will end, the site will revert to something stable, and the site will break a year later when the experimental feature is standardised.
alex: Yes, that is a risk.  But it's better than where we are now.
...And the goal of the traffic threshold is to limit the possibilities.
peter: I just hope we don't get into a case where, 2 years later, "oh they're sending me a key for this expired experiment, and now I have to change my behaviour"
travis: Agreed
alex: Small group. We care about you, and we're giving you another way to do it.
...We expect to see this go out with a couple of new features (javascript APIs) end Q1/early Q2.  Local font access is probably one of the first.
travis: It doesn't sound like we have concensus on this text.  We could at least make a statement akin to what you said at the beginning, Alex.
alex: If we do nothing, events will over take us. And that would be great.
travis: okay
Peter: So we'll keep an eye on it, see how it evolves.  As we gain wisdom, we can disseminate later.
hadley: I do like that watching this will give us some actual data, on which to make decisions...



## EWS Blog Post

Intro
 - (event page: \url{https://ti.to/torgo/ews-melbourne/en)}
 - goal of EWS events
 - what happened
 
 We had a perfect event - lovely Wifi, great catering, well organised and everyone was very happy that this end of the world got noticed. (?)
 

   * - thanks to folks who provided venue and snacks
   * - lightning talks
   * - sessions - links to session notes (\url{https://github.com/w3ctag/wiki/wiki/2016-Melbourne-Summit)}
 - summary of what we learned and took away

   *  - community engagement FTW - note on provisional next EWS timing/location
















