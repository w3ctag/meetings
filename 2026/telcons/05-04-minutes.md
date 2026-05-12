# TAG Minutes Week of 4 May 2026

This was a document-focused week, but we had a plenary with ad-hoc topics, listed below.

Present: Christian, Ehsan, Marcos, Heather, Sarven, Brian, Jeffrey, Matthew
    
Regrets:

## [Explainer-review skill](https://github.com/w3ctag/explainer-explainer/pull/39)

Marcos: We should run this on some explainers we've already reviewed.
    
Heather: Why would it be bad to run this as an experiment? I can't think of anything. Like the idea of trying it on things we've done, and review that. Nothing wrong with experimenting.

Jeffrey: Should we run this in the private repo?

Heather: Sure, Why not?

Jeffrey: Will try to set that up.

Christian: Seems like an interesting experiment. Like the idea of starting internally first, checking with reviews we've already done. If it helps save us on resources and gets people information faster, that might be a good thing. 

Jeffrey: Consensus. Will integrate Marcos' suggestions and then merge it. 

Marcos: Will send an updated script. 

## [Interest Target](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058)

Matthew: I have enough to write a comment to propose to everyone. 

Jeffrey: The current draft comment says this is not implementable on other platforms. After the recent iteration, it is implementable but WebKit doesn't like the resulting UI. Is that correct?

Brian: Luke and I were involved in OpenUI from the beginning. There's good thought behind this and there was work to make compromises. So, generally supportive. 
    
Christian: This is tricky. By itself it's fine, on desktop it's ok, but the show details on mobile doesn't feel like a great UX. Would be cool if you have access to longpress. Would suggest no consensus.

Marcos: The main thing is what I outlined in the comment - this option lands up in a menu and if the handler isn't set up properly, it shows weird things. It is confusing for users. Everything else has a defined action, but this defers "show details" to the web page, which may result in unexpected behavior. It's a break in the expected contract.

Jeffrey: We have websites that do things on hover, and this lets mobile users have access to that. There is the interest button that goes with this that provides a button to go with the target (for things that don't have hover) and the browser can show something better. There has been a desire to be able to add things to the menu (overriding the right-click menu), but that's a different proposal. 

Marcos: Theoretically gaze-based and mobile systems can do the same thing, but it would only work for things like highlights and basic effects. It can't trigger an event, so it can't run a script.

Jeffrey: It can show buttons, and that can include "show details". Scripts can run when clicking that button.

Marcos: But you don't want to show people what your interested in. 

Jeffrey: The proposal is to fire the interest event when you click the button, that grants consent to show the event.

Brian: I have custom elements that did this a while ago, using a media query to determine what to show and act on. But it doesn't show up in sequential focus. The work to try and make this as much like a button-like thing when you need it so you can activate it on some device, tries to map this to a basic click.

Marcos: With CSS, you don't need the interest thing because you can detect what kind of device your on and render a button if necessary. Do we really need this, then? 

Sarven: I think I agree with Christian. What also concerns me is the accessibility of it and the affordance that comes with hyperlinks or buttons, what people are accustomed to. This inserts another affordance in between what we visually see / hear and the action. There is some convenience to it and people might need to just learn new behavior.

Jeffrey: The explainer goes into what people are already doing in this area. Lots of sites are doing things on hover; GitHub is one people are familiar with. We discussed doing this as a link preview. The reason to do it natively is that people get it wrong - they ignore keyboard navigation, do nothing on a touch screen, get accessibility wrong. The touchscreen and immersive UI are not perfect, but they let those surfaces participate in UIs designed for the standard user with a moust.

Matthew: Agree with Jeffrey. Would add that this is quite congruous with the trend to make more declaritive stuff in HTML and not have to do JS. If we can get this right on other platforms, that would be good. Wikipedia does this as well so you don't have to drop down to the footnotes. The idea of the event is interesting as well as it takes us to more abstract UIs. We agreed in a previous TAG that the use case is a good one and that it is not the same as a pop-over. The button approach would be sufficiently privacy preserving, it's just whether it's acceptable and fits platform conventions. We could say we don't have consensus but you might want to explore these things. 

Brian: Agree with Matthew. None of this stuff is new or taken lightly. It has had participations from multiple accessibility specialists. 

Marcos: The CSS nor the event is going to give you accessibility. What gives you the accessibility is the popover. HOw does this buy you anything with accessibility? At the end of the day, you'll still need popovers, CSS, HTML to get things done. How does this buy you anything but the interest part?

Luke: The interest part is a lot of the accessibility. The accessibility mappings are augmented by having interest target. 

Sarven: It is a design pattern coming up, and if this is a way to have smaller, common patterns emerge, maybe it does make sense. 

Marcos: The things being described are the happy paths. What I'm looking at is the less happy path, when it gest into naive hands that implement it incorrectly. How can this be misused and abused? If it is framed in terms of accessibility, the tradeoff is privacy. 

Matthew: it's an implementation detail, but it's like ARIA; it just works. It is important to consider how this might be misused. The primary examples we're seeing in the explainer is popover, which can be done differently. There's more likelihood that people will get it wrong if we don't do this than if we do. In terms of privacy, we've established we can do this in a privacy preserving way, it's just that the UI is clunky. It does sound like we don't have consensus, but I'll try to be slightly clearer in the comments to capture this.

Sarven: Why the name, "interest"? I'm worried that this can trigger other things by proximity that they didn't intend to. Is there more documentation about that?

Jeffrey: You can experience the goal on GitHub, you can click [edit after the meeting: this should be "hover"] on someone's username and see what this is supposed to do. The pitch section describes how much easier it is to be careless without this event.

Sarven: Is this more like a GET? Is it intended to be a safe operation?

Jeffrey: It doesn't trigger an HTTP request. It should be safe. Developers should not post (it's not that they can't).

Sarven: I'm concerned that some of the events should be better isolated. I'm hoping for documentation that explains that part. 

Christian: My opinion has changed slightly. The use case looks fine and interesting. If I think about how I would use that on mobile, what would I be expected to do? Would I really longpress a username and then say show details? How would I know this action is available? But this is probably a UX challenge.

Luke: For the username example, yes, the UX is not perfect. There is a context menu you can work with. The buttons on Android you don't get the intervening context menu. For the buttons, it is common on Android to longpress on something, but "show details" in the link is not perfect. As for the event, it is not providing anything we don't already have. It's not uncommon to want to pre-load a page when one hovers over a link, for example. I don't think there is anything super dangerous here, which is why it's not documented. The concept is an amalgamation of things already exposed. 

## Open source implementations

Sarven: The idea was whether the W3C should require open-source implementations for spec features. Right now, the W3C does not say anything about open/closed source. We learn from implementation experience, and some of that flows back into the group in different ways. Some contributors provide open source or reframe explainer information to be input into the group. What's missing is public verification of implementations. If we value that quality towards adequate implementation experience, then we should consider this. There is also the possibility for the public to re-run implementation reports independently, so even if the creators are no longer with the group, it still makes it possible to run these independently and provide the latest status of conformance. 

Marcos: This was not my read at all on what they were asking. My take on this was that they wanted to throw money at Bikeshed and Respec. The testing side is covered by WPT on the browser side of things. This was about open-source projects that support the web community.

Jeffrey: I am skeptical of adding an open-source requirement to implementation requirements. 

Sarven: I'll create an issue so we can discuss further.

## DAS
