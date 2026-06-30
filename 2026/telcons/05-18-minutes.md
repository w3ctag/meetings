# TAG minutes, week of 18 May 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/05-18-agenda.md).

## Plenary Session - [2026-05-19](https://www.timeanddate.com/worldclock/converter.html?iso=20260519T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Sarven, Brian, Christian, Xiaocheng, Heather, Ehsan, Hadley, Lola, Luke, Matthew, 

Regrets:

Scribe: Heather

### [design-principles#614: Open source implementations as a baseline requirement for adequate implementation experience](https://github.com/w3ctag/design-principles/issues/614) ([Github](https://github.com/w3ctag/design-principles/issues/614)) - @csarven

Sarven: Nothing overly new here. Tracked the slack discussion started in the last meeting.

Hadley: Did you open up an issue in the Process CG?

Sarven: I can. Thought we suggested starting it here under design principles. We did pass some recommendations from DAS that we hoped the charter template would address.  Does anyone have additional thoughts or input?

Jeffrey: I don't think this is worth doing. Closed source implementations are fine for web standards. Still, worth raising and if the rest of the TAG agrees, won't block.

Brian: Agree with Jeffrey. Layers of this argument have been going on a long time. The point is probably more nuanced. What are you trying to do with this? Recommending that this is a good practice seems reasonable, but not sure what requiring it accomplishes. 

Hadley: I like the three bullet points of what OS implementations allow. They should be encouraged. I would be concerned about making this policy because there is a possibility that is easier with OS where the implementation is something someone just hacked together by one of the editors of the spec. 

Lola: Sarven's proposal isn't saying not to consider closed-source implementations. It is saying closed source implementations will have a different weighting when it comes to a Recommendation. Open source is one of the ways to address the issue of how do we know if something is actually implemented and deployed to the web. Is OS the only way to do that? Ultimately, this is a Process question.

Sarven: Some charters say at least two implementations per feature, passing open test suites. Suggest saying that those two should be open source; there can be more implementation and those can be open or closed. The W3C recommends all sorts of things like royalty free specs, OpenStand, etc. We have expectations for what the community wants to see in terms of open source, unrestricted access to references (e.g., https://www.w3.org/2012/08/open-stand-w3c.html , https://www.w3.org/guide/process/tilt/normative-references.html#orgs ). So making this part of the expectation aligns. Want to separate the notion of shared code and the licensing on that code. This issue is about the latter, seeing the code and being able to use the parts that are useful more broadly. It also makes verifying tests were passed easier. And all of this is the baseline, not the exclusion of closed source.

Jeffrey: All of those aspects are good, and suggesting each of them to the Process is a good idea. Right now, making this requirement would not slow down the browser side of recommendations as all browsers are open source. Not sure about the other specifications produced by the W3C. Often I would say we should ratchet the requirement, to ensure we don't regress. But the OS ecosystem is under a lot of pressure and hasn't figured out how to be sustainable. Worried that something will shift in the ecosystem and the software we use will no longer meet the definition we use for OS. I don't want to put a stake in the ground and have that be in the wrong place.

Xiaocheng: I don't think we should add an open-source requirement; it's tackling the wrong problem. It's not that we have too many independent implementations and we want to be pickier. We actually have too few and we want to encourage more. I don't see how an OS requirement benefits us. The way it might discourage implementers does more harm.

Hadley: Echo what Jeffrey and Xiaocheng are saying. Someone is eventually going to have to pay for the OS maintainers. The harder we make it to create standards, the less our members will be happy and will stop trying. 

Heather: Was agreeing with Jeffrey until he said not to put a line in the sand when things might change. Things will always change. Don't think it'll change so fast that we couldn't do something now, and as it no longer applies, recommend something different. Unless we had evidence that the unknown future state was going to be by the end of the year.

Sarven: One counterpoint about funding and resources for OS or limiting implementations: wouldn't what we're suggesting actually have the opposite effect? If OS is the bar, wouldn't that increase the expectation of more OS development and therefore more funding from those orgs looking to grow OS? If OS was not a requirement, then you still have to answer the question of why bother doing OS in the first place.

Hadley: Maybe. We have always been a community of secrets; it echoes the idea of people coming to meetings with their own agendas. We have a level playing field where people can leave those secrets at the door and have a rich conversation. Would the web be poorer if that was no longer possible?

Brian: Would the concerns be resolved if the TAG created a note around the kinds of value that the communities gain from different kinds of implementation experience and that strongly supports OS, interoperable, two different maintainers, two different code bases, that are openly licensed?

Sarven: I am glad we are spiritually aligned, even if we have practical challenges. We do have some power here to make suggestions and indicate our position. So, would appreciate if we had some form alignment.

Jeffrey: Post a TAG position of support. But we need to be clear as to what we mean by OS. Not all the restrictions in the OS definition (https://opensource.org/osd) are ones we want to apply to implementations. 

Hadley: Sarven you are welcome to draft something. Not sure you will get TAG consensus, but you are still welcome to try. If you want to have the discussion as an individual with the Process CG, you should feel free to do that. 

Sarven: I will propose something simpler to the TAG. Will pitch it for a future plenary. 


### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: Had a good discussion when we talked about this last. We have a draft comment that indicates we don't have consensus but suggested a way forward. One way privacy can be preserved is for the UA to create a button the user can press to express interest.

my question... a privacy-preserving way of doing is is for the UA generates a button, and you push that button to say you're interested in this element. So you know what it's doing. I foudn the discussion the CSS working group had was a little bit circular.

The CSSWG approach was to provide a pseudo element for the button (https://github.com/w3c/csswg-drafts/issues/12437) - so more control (and responsibility) given to the web developer.

Luke: The UA provided button they can show, and the CSS thing, are two ways of solving similar problems but not the same. The CSS button is largely under the developers control and helps the user discover the feature (it is not discoverable in some scenarios). It might also solve some accessibility issues, the existing implementaiton regarding voice control, but I think it's up in the air whether that's stripping needed or not. The UA part is something we already have for links. The VisionOS style is a UA style thing like that. I think the CSS one is better because it's under the developer's control and. might make the feature easier to use. But UI is up to UAs in general.

Matthew: Responding to Luke, how does it help the user discover that they an express interest in something to both require and rely on the web developer to style it in such a way that it's not hidden and make it obvious what it is, whereas if the UA controlled it, it would be consistent across the whole web platform. The entirely-UA button might not be in the accessibility tree, which isn't great. But this button is for people who are not using any other way to interact with it.

Brian: Some of this feels circular because it is: what is best is for it to be controlled by a platform and be consistent, but also we know that developers already are trying to provide this by building their own. They don't look entirely consistent. If they don't have an ability to style, you wind up in a position where people will continue to use their moderately terrible solutions. How do we meet both needs, to make it appealing enough? Pseudo-elements can be limited in their styling, but I don't know.

Luke: +1

Jeffrey: I don't see whether the interest button is available by default for platforms without a hover. If yes, then the developers could tweak the styling. If it's invisible by default, developers won't remember to use it.

Matthew: Agree with Jeffrey, and appreciate what Brian said. I was only expecting this to appear on platforms where it has to. What you're describing is that it's not just like how it works on GitHub where you hover over something and you get something. You might have other sites that will use this. But developers do forget to apply accessibility principles. 

Luke: Last I heard, this would be opt-out, not opt-in. We shouldn't make it easy for developers to make mistakes, but they will. We want to make the problem space easier for developers that want to do it right; we are not trying to make things easier for developers that don't care. We can put warnings in dev tools and MDN, but at the end of the day, if the developers don't like the look of the button, they won't use the feature, and we'll be in a worse place. 

Hadley: Matthew will try to revise the comment.

### [design-principles#280: Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280) - @xiaochengh

* https://github.com/w3ctag/design-principles/pull/592

Xiaocheng: Suggestions: Event names when using a verb should only use present tense. That's mostly how its done now, though there are some archaic examples.

+1 from Hadley, Brian

Xiaocheng: There is a PR to the design principles for this. The remaining recommendations are more controversial. I am a bit uncomfortable with the symantics of the event name - has something happened or is something about to happen and we have a chance to intervene? There is no consistency in how this is handled.

Luke: With the before prefix, it is syncable and cancelable. Cancel is synchronous, Close is not. It is not super consistent even with moder features. Present tense vs past tense is fairly settled, but the rest will require more research.

Jeffrey: We need a full PR to land this, but it sounds like we have agreement from the group. We'll review that, double check with the group before finalizing.

Brian: There are two separate PRs, right? We'll focus on the tense first.

Jeffrey: Encourages Xiaocheng to be more aggressive. We know it's not consistent, but perhaps say people should try "X" so we can improve in the future.

Hadley: Reminder to update the editors to that as well. 





### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)



### Ensuring a sustainable future for Standards Development Organizations (SDOs) - @jyasskin

Jeffrey: I have been hearing concerns as to whether the W3C is going in the right direction and whether it can be rescued. The TAG is part of the W3C so we should work towards fixing that, but we're also responsible for the web so even if the W3C falls apart, we need to support the future of web standards development.

Hadley: We will need to come back to this and think to what parts are ours to solve for. 


## Pacific Breakout (Asia / Australia / West America) - [2026-05-20](https://www.timeanddate.com/worldclock/converter.html?iso=20260520T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Brian, Dan, Jeffrey

Regrets: Christian

Scribe:

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu

Brian: Heather made a comment. Should we discuss?

Jeffrey: Think Heather's "functions" are the way we define "user agent".

#### [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu



#### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu



#### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu



### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan

Jeffrey: Will merge Marcos' draft, with a couple tweaks.

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan



### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @dandclark, @xiaochengh

Dan: Lots of nits, but this kind of thing has been done before. Will workshop with Xiaocheng. Overall they said "thanks but no thanks". Will suggest that they consider when is the time to add an object model, and consider whether there may be a time when this property can go away after implementations have done the work.

### [user-agents#47: Can we cite user agents in normative specs?](https://github.com/w3ctag/user-agents/issues/47) - @jyasskin



### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark

Not fair to ask Dan to do all the drafting. Jeffrey to do a pass and propose a comment. Probably basically what Dan drafted.

### [design-reviews#1214: [wg/math] Math Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1214) ([Github](https://github.com/w3ctag/design-reviews/issues/1214)) - @christianliebel

Christian/added before the meeting: Working on it.

### [design-reviews#1215: [wg/wot] Web of Things Working Group rechartering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1215) ([Github](https://github.com/w3ctag/design-reviews/issues/1215)) - @jyasskin

Jeffrey: I drafted a comment. No objections heard in this breakout. I'll post to Slack, and post the reply if I don't get objections by Thursday.


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

Assigned several issues. Declined the Web Transport charter review. We marked several issues as "propose closing" to let Europe claim them before we decline.

Marcos: Browser Testing and Tools Charter: would be nice if the WG provided more formal guidance for how specs should integrate with WebDriver BiDi. Currently specs have to cargo-cult eachother.

## Atlantic Breakout (America / Europe) - [2026-05-20](https://www.timeanddate.com/worldclock/converter.html?iso=20260520T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Brian, Lola, Mike, Jeffrey, Dan, Matthew

Regrets: Ehsan, Christian, Heather, Luke

Scribe: Jeffrey

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Lola: Let's schedule this for the plenary next week, and if we can't find a co-chair, stop working on it.

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Brian: We talked last night and decided we need to reload user-agents#36 that Heather commented on. Jeffrey was going to check if the wording already satisfies Heather's comment.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Jeffrey: working on review skill with Marcos. Marcos updated a draft ; I need to make some edits, then merge it. And then we can get feedback.


### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

Mike: Is feedback useful since it's shipping?

Lola: We can decline to review things if for whatever reason we don't want to review it. We'd write a comment. However, even when something has shipped or is close to shipping, our feedback can still be helpful. It's good to have a written record of what we thought, even if it doesn't cause implementation changes.

Jeffrey: Eevn though this is close to shipping in Chrome, it's not close in the other browsers. There's a window to effect their implementations, and that could impact Chrome.

Luke: FWIW, it's not shipping in Chromium. The I2S was paused to extend the Origin Trial for ~3 versions. 

Mike will continue reviewing.

### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow

Brian: Lot of conversation happening in WHATWG today. 

Luke: On my TODO list. Intermediate response saying we want more thought going into behaviors other than the submit button. Lots of ongoing discussion in WHATWG. Don't need to reference that. Let them play out?

Brian: Could include Anne's comments. In line with ones we had, about decorators, being a weird middle ground.  Where it's very specific but also too general, in a weird way. You made the point that nobody's advocating doing every atom as its own thing, but we need to break out some of them.

Jeffrey: I think we should endorse the bits we agree with. We shouldn't let thatplay out before we comment, but we can say, "please continue in this direction."

Overview of what this is:
    
Luke: This is a way to give custom elements behaviors that are currently reserved to built-in elements. Gone through quite a few iterations. Current iteration names behaviors, and includes them using "attach internals", which has a static list of behaviors. The one that's concretely proposed is the "submit button" behavior. That's the only concrete proposal, which is a piece of feedback. 

Brian: Addressing Jeffrey. Don't know that they are getting the feedback. Discussion is happening, but the people might not be there, getting the feedback directly. 

Jeffrey: We could ask them to attend.

[In chat, Dan says proponents are attending meetings.]

Brian: Point to the public discussion, and say we agree.

Lola: Found the Security & Privacy section... Adding form submission ... they say all security checks apply. Wouldn't be any new security concerns? 

Luke: Think because it's currently imperative, they can trigger form submission through JS. Maybe there are subtle details about the JS APIs and how they interact. Think that's something that, depending on the behavior, there are things they'd need to think about. Concrete example from WHATWG chat: if we introduce hyperlink behavior, that probably shouldn't be able to navigate to `javascript:` APIs. Because sanitizer API can't know it's a hyperlink and can't know to remove those URLs.

Luke: Will ask for more concrete examples and WHATWG examples.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Lola: I read Torgo's post. It's helpful to a certain extent. Distinction ... "what the web is" is more obvious, but distinction between "web" and "web platform". 

Luke: Question is, can we define this? I mentioned some of this last week. Has there been thinking about web-interoperable runtimes? Node, Deno, Bun: where do they fit in? Web has the origin model. Deno might have more of that. Has a permission model. Think it has origins. Doesn't have CORS. Interesting to touch on them. Maybe just to say they're out of scope.

Jeffrey: I think the distinction between the "web" and the "web platform" is that the "platfom" is the software and the API s that the content can use.

Lola: Sounds reasonable, but want to think more.

Brian: Context was XSLT, which raises XPath, X*. What about EPub? Linked Data? 96 closed WGs, where a lot of them are about RDF or Semantic Web or X. Services. Today there are 8-10 open ones about things that aren't in browsers. RDF, SPRQL, Canonicalization. Stuff that's in between, or we don't know yet. Attribution is in the browser but also needs a service. Key to this question. Are there labels we can put around those things to help us discuss them. Don't be offensive, but say something useful. For the W3C, it's important to come to grips with this. The W3C itself seems to have deprioritized them. Biggest thing the W3C has, budget-wise, is Team Contacts. 25% of budget? None of those groups have a Team Contact. That's why this is interesting. Verifiable Credentials? Social Web isn't in the browser. Servo has an experiment building AT Protocol into the browser.

Mike: I'm thinking about it, after the reading, is aligned with what Jeffrey said, which doesn't get to what Brian's saying about what makes the cut. Mental model is that the Web is a deployment of the Web Platform on the internet. Matches models of set-top models, Netflix working on "their" web platform. Has URLs but not on the internet. Doesn't address Brian's point about "what is the web platform?" Seems like the W3C has a role to play. Someone has to steward the definition of Web Platform for it to be useful on the non-Internet deployments

Jeffrey: Yeah. I think that Brian has a deeper question there: what should the W3C work on? That isn't necessarily answered by, "what is the web/web-platform?" We should maybe elaborate what we want to use this question to do--rather than just the philosophical value of the question.

Brian: 100%. I'm relaying the question from Dan. It was asked in the context of some people asking to deprecate XSLT. People said it's "part of the web platform". Is it? Maybe helpful to articulate this. There's some distinction. Maybe not part of the Web Platform. Maybe we need more terms.

Lola: Quesiton you're getting at ... 2 questions: "What should the W3C consider to be the Web Platform?", vs "What is the web vs web platform?" Your question is suited for the Technical Strategy Task Force.

Lola: Drop this from the agenda?

Brian: I'll keep pondering, and will bring it back if I come up with something. Other people could work on it.

Lola: Bring this to the wider W3C? 


### [design-reviews#1205: WG Revision: MathML 4](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1205) ([Github](https://github.com/w3ctag/design-reviews/issues/1205)) - @jyasskin, @matatk

Jeffrey: I have draft comment in the private brainstorming repo. What do people think?

Matthew: I like it. It is nice.

Luke: Maybe not a quesiton for people here. What is MathML 4, if we have MathML Core? Is there something MathML4 is doing differently? "Why?"

Brian: There's a lot of MathML that's outside of browsers. A lot of tools were built with that in mind. Same question as SVG. There's an SVG set that works on the web, but also Inkscape. Feelings about the way they did this `intent` thing, and the amount of discussion on that.

Jeffrey: For intent in particular, it seems like it is promising for assistive technology. Even if all of MathML 4 doesn't land in browsers, but this piece might. I don't know that we need to question that aspect of it since it seems like a useful addition.

Brian: Then it belongs in Core. That's the trouble. Answering what 4 is. MathML 3 was a work of fiction. Aspirational. Included a lot of stuff that nobody implemented. Lot of stuff it dictated was incorrect. MathML 4 is trying to ground it in reality, and reconcile it with Core. Points to Core for things Core does. Saying, "We're that and some more." Also using it as incubation for what we'd like to see move over to Core. That's weird since it's a follow-on to an actual-REC.

Luke: Why isn't this a piggy-back off Core? Think that's the way to go. AT doesn't work off raw HTML

Brian: There's a significant amount of stuff that was real in MathML3, but didn't fit in Core, which was the stuff we really needed to get done before we could consider more. MathML4 is minimal new stuff, really just `intent`.

Jeffrey: Maybe the discussion here should also say, "please do this as an incubation rather than putting it directly in the spec." We think they should have done it differently, but we're also generally happy with the design. I'll make that change and post it.

Lola: Sounds good

Matthew: That sounds fine

### [design-reviews#1209: [wg/ag] Accessibility Guidelines Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1209) ([Github](https://github.com/w3ctag/design-reviews/issues/1209)) - @jyasskin, @matatk, @hlflanagan

Jeffrey: I posted a draft comment that just says, "We don't see any architectural issues with the charter"

Lola: That seems fine

Jeffrey: Okay, then I will post that.

### Addition from Matthew: can we look at the `interesttarget` comment I proposed?

https://github.com/w3ctag/design-reviews-private-brainstorming/issues/118#issuecomment-4500288046

I am away from 05-21 to 05-26.

Matthew: Can't get Marcos' view on this call. Tried to articulate what we don't have consensus on. Incorporated my understanding of the ::interest-button thing, which was greatly helped by Luke's explanation. Hoping that gets us closer. Happy for someone else to post if I'm not around. Think everyone had reasonable concerns.

Jeffrey: I will read it asynchronously.

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini



### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini



### [design-reviews#1190: Incubation: Cryptography usage in Web Standards](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1190) ([Github](https://github.com/w3ctag/design-reviews/issues/1190)) - @toreini, @lolaodelola

Lola: Ehsan posted to the Security group's repo, without response. Marking 'pending'.

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini



### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1128) ([Github](https://github.com/w3ctag/design-reviews/issues/1128)) - @toreini (pending >= 6mo)


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

Jeffrey: There were a couple that we left open on purpose in Pacific because this group might want to adopt them. There are four issues total in triage.

#### overscroll: https://github.com/w3ctag/design-reviews/issues/1228

Luke::Intent sent. Being reviewed by CSS. Decline?

Jeffrey: There was a presentation at BlinkOn that made it seeem that this was a piece of a complicated way of doing "drawers." That bigger system that this was part of seemed like it was worth looking at. Like, with carousels, the pieces looked fine but the overall system wasn't quite right. We might want to look in that way, but I don't know whether I have the expertise to actually perform that review.

Luke: Yes, this is part of a declarative overscroll thing from OpenUI: https://open-ui.org/components/overscroll-actions.explainer/. This is useful for that, but is a standalone isolated bit, which is why it's shipping as it is. It's useful on its own. No submission for the overall thing yet. Think it's ok to say that this piece is fine. Then do the larger thing when they request it.

Lola: Are there accessibility considerations for this? None in the explainer. Even a "no accessibility considerations" would be helpful. The explainer is short and assumes a lot of knowledge. Don't know what the technical terms mean. Can decline to review, but part of the reason is that there's not enough information.

Luke: Can comment that, and privacy and security. Can say there are no considerations, but should have it.

Matthew: +1 to please have an "accessibility considerations" section, even if it's empty. That shouldn't be special. Should have "all of them". Internationalization might be "obvious", but if there's a possibility, should encourage that too.

Jeffrey: I doubt it's obvious because right-to-left is quite likely to be affected by overscroll.

Luke: We should always encourage those sections. Might be obvious to me, but if someone else is reading, they should know it's been considered.

Matthew: Worth mentioning in the explainer explainer?

Jeffrey: I think it's already mentioned

Luke + Lola assigned.

#### [Flex-wrap: balance](https://github.com/w3ctag/design-reviews/issues/1227)

Lola: Missing those sections. Internationalization?

Jeffrey:  Line wrap verus word-wrap balance which is already shipped. It's just simpler. I think this is happening in CSS, which is why we weren't too worried about it. It's already in the CSS draft.

Lola: Think we can trust CSS to do their own thing, but sometimes things slip through that we should have looked at. But if folks feel like it doesn't meet that requirement, ok with declining. If we decline, shouldn't say it's because it's happening in CSS.

Luke: Intuition is that this is a modifier on the flexbox layout that isn't necessarily that different from a combination of other things flexbox already has. Think CSS will make sure layout is coherent. It doesn't introduce something new. CSS grid-lanes makes sense since it's a new paradigm. Something like this, modifying an existing thing in a relatively small way, seems fine.

Brian: Given what it is, doesn't seem like much architecturally to review. 

Jeffrey: I can draft a comment. I think it should include, "please do include the 'considerations' sections." The proponent did a lot of work that I want to be sure to recognize.

#### [Incubation: Lightweight and Conditional Tracing for long animation frame timing API](https://github.com/w3ctag/design-reviews/issues/1224)

Jeffrey: I believe this will be in web-perf eventually, but it's currently in incubation.

Lola: Anyone want to take this? Hearing nothing, I can ask in Slack or in Eurasia tomorrow.

#### [Other Spec Review: Single-Axis Scroll Containers](https://github.com/w3ctag/design-reviews/issues/1222)

Lola: Also CSS. To Eurasia.

## Eurasia Breakout (Europe / Asia / Australia) - [2026-05-21](https://www.timeanddate.com/worldclock/converter.html?iso=20260521T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Marcos, Ehsan, Lola, Xiaochengh

Regrets: Matthew, Christian

Scribe: Lola

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh



### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel, @xiaochengh

Christian/added before the meeting: Closed! :)

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

Luke: Posted draft comment, need feedback from Matthew and Xiaochengh. Jeffrey mentioned being more concrete in the comment so I'll expand. Waiting on Xiaochengh to confirm his questions have been addressed.

Hadley: External deadlines?

Luke: I think so, I don't see any shipping indications for any time soon.

Hadley: Ping Matthew and Xiaochengh?

Luke: Will ping on slack.

Ehsan: Matthew is on leave until next week.

Luke: It's more Xiaochengh I'm waiting on.

Xiaochengh: *reviews comment*

Luke: It probably needs fleshing out

Xiaochengh: Philip has addressed my questions in the meeting. We can close as satisified.

Luke: Matthew mentioned on-going accessibility convos, we should wait for discussions to pan out before we resolve as satisfied. There are concrete accessibility issues.

Marcos: This has a lot of impact on various things, including PEPC proposal. Do we have feedback from implementers? We should check Webkit and Mozilla positions. You can't use PEPC if you're using this due to incompatibility.

Luke: There are no standards positions at the moment.

Marcos: Anna has given feedback. I'd push hard to get standards position before we give our position. I will bug Anna and others who know the area. I want to avoid interesttarget issue happening again.

Luke: I've added multistakeholder label. I will incorporate that into comment.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh, @lukewarlow

Luke: It's a review for a thing that's Baseline "newly available" so already shipped (Anchor Positioning Level 1). I have some concerns with  position-visibility property. I can't evaluate implementation, even in spec unsure it address usecases. I will write draft comment that summerises my concerns. `position-visibility`  was added later and also very buggy so there may still be time to change. The idea of position-visibility allows you to address popover sticky header issues.

Xiaocheng: Is the sticky header issue fixable? is it a spec or implementation bug, or something fundamental with anchor positioning?

Luke: I think it's a spec bug and not just an implementation bug.  I think intersecion observer v2 has this concept of visibility, and I think we have the mechanics for it. it's a matter of specying nad implementing to meet those mechanics. I htink it's been designed wit ha specific use case in mind, where you ahsomething anchored but not directly next to the anchor, and the anchor goes off screen and you want to get rid of the info box about the thing. Whereas I imagine it's where you have stuff where they are next to or close to each other, and one gets obscured and you wnat to hide the other.

Hadley: Xiaochengh how do you want to review Luke's comment?

Xiaocheng: I'll look at his comment.


### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Xiaochengh: We only have accessibility concerns, wait for Matthew.


### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Lola: there were comments, I responded in the brainstorming issue. i don't think i've received a response. 

To summarise, this person came back addressing the concernes we had. the syntax for this was using cover and contain, which is being used in other parts of CSS that have nothing to do with animation, things like images and media. They responded that they hadn't considered that, and they aren't using those words for animation. I agree it's probably out of scope for these folks to address that. but i'm not convinced with their whole explanation, becasu they say there is a lack of developer complaint about using these words — which isn't user research. i gave some suggestions of potential research avenues.

I don't think this is blocking, but I would like to know what other people think. I think it's weird that the CSS working group haven't picked this up. 
Recently they had an issue where they named something masonry and they've changed it to grid lanes, hwich means updating developer docuemntation and confusing them temporarily. I'd like to avoid doing that frequently. 

Marcos: we could call in the CSS WG folks

Hadley: i agree, or send the chairs a message.

Lola: I can ping Alan Stern.

Hadley: let's leave this open until you've talked to them then. Should we also put a concluing statement on the issue?

Lola: I'd like to hear from Matthew first. He's been the main person interfacing with them. 

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

*skipped*

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

 *skipped*


### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

*skipped*

### [design-reviews#1206: Other Spec Review: OpaqueRange](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1206) ([Github](https://github.com/w3ctag/design-reviews/issues/1206)) - @matatk, @lukewarlow

Luke: I posted draft comment to resolve as satisfied. Jeffrey and Brian have thumbsed up, we should post if no objections. Matthew agreed with overall sentiment.

Hadley: You're not expecting red flags for Matthew?

Luke: Yes

Hadley: Time pressure?

Luke: They've sent intent to ship

Hadley: Judgement call for you, if you think he will agree post or if concerned send slack to allow him to respond.

Luke: I'll do that

Ehsan: I can help nudge if you want

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk, @lukewarlow

Luke: Waiting on Webkit to provide position. Matt and I are happy with feature. 

Hadley: What is it?

Luke: allows grouping of elements into single tab stop. instead of tabbing 10 elements, you can tab in and out of groups. you use arrows instead of tabs, useful for menus, etc. HTML feature allowing you to write without JS. Users don't like tabbing through every menu item, takes a lot of JS to tab groups, this allows you not to. Doesn't change focus of elements. Buttons aren't focussable by keyboard in Webkit, and will remain that way. We're waiting.

Hadley: Webkit team involved but no standards position?

Luke: they've left comments

Hadley: timeline?

Luke: It may have shipped in Chrome

Marcos: for webkit, Anne has looked at it and like the idea, I'll ping Anne for final position. The actual feedback may be coming through WHATWG discussions.

Luke: I think there was comment around testing, I don't think TAG needs to worry because it's a pre-exisiting testing issue. WPT doesn't have way to account for WebKit focusability issue.

Hadley: Please leave public facing comment to explain we're waiting for WebKit stands position so that it's clear to people looking at issue why progress has stalled.

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

*skipped*

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

*skipped*

### [design-reviews#1153: WG New Spec: Direction feature for `scroll-state()` query](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1153) ([Github](https://github.com/w3ctag/design-reviews/issues/1153)) - @matatk, @xiaochengh (pending >= 6mo)

Xiaochengh: We gave generally positive feedback with questions and have had no response. We should close as timedout.

Hadley: Are we unhappy if no changes?

Xiaocheng: No

### [Incubation: Lightweight and Conditional Tracing for long animation frame timing API](https://github.com/w3ctag/design-reviews/issues/1224)

Lola: yesterday, we went through the issue triage. This issue, and the next, we couldn't find anyone to take on in Atlantic breakout. So we wanted to assign them from this breakout. Anyone?

The first is performance-based. It's looking at measuring the performance for animations. 

Xiaocheng: I will look at this. 

### [Other Spec Review: Single-Axis Scroll Containers](https://github.com/w3ctag/design-reviews/issues/1222)

Xiaocheng: I will also look at this. 

Luke: I'm interested as well. 

