# TAG Teleconference
#### 16-18 December 2024

---

## Agenda:

### Breakout A (California / Europe)  - [2024-12-16](https://www.timeanddate.com/worldclock/converter.html?iso=20241216T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* UA finding draft
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman
* [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman
* [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

### Breakout B (California / Australia) - [2024-12-17](https://www.timeanddate.com/worldclock/converter.html?iso=20241217T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Improve the run-to-completion principle.](https://github.com/w3ctag/design-principles/pull/536)
* [Add a section about looking for guidance in other specs.](https://github.com/w3ctag/design-principles/pull/542)
* [CSS advanced attr() function](https://github.com/w3ctag/design-reviews/issues/513) - @hober, @dbaron, @plinss
* [Early Design Review: Allowing First-Party SameSite=None Cookies in Sandboxed Contexts ](https://github.com/w3ctag/design-reviews/issues/1004)
* [[Handwriting] Add Handwriting CSS Value](https://github.com/w3ctag/design-reviews/issues/1018)

### Breakout C (Europe / China) - [2024-12-18](https://www.timeanddate.com/worldclock/converter.html?iso=20241218T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion
* [EPUB 3.3 Recommendation with Candidate Corrections  2024-10-17 > 2024-12-19](https://github.com/w3ctag/design-reviews/issues/1006) - @rhiaro, @hadleybeeman
* [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017)

### Plenary Session - [2024-12-18](https://www.timeanddate.com/worldclock/converter.html?iso=20241218T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Dan, Matthew, Amy, Jeffrey, Hadley, Yves, Tess

Regrets: Lea


### UA finding draft

Peter: Go for it.

[Posted to https://github.com/w3ctag/user-agents ]

### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

Jeffrey: we should answer the question about complexities of popin approach

Dan: I channelled discussion.. 

Jeffrey: I think the complexity is the questions about how to do the UI to present the fact that it's partitioned but still looks like a popup. I think that was interpreted as developer complexity but it's UI complexity

Dan: yeah. We don't want to specify UI..

jeffrey: important for specs to give an example of good UI. We don't specify UI, but it should be clear it's implementable with good UI.

Hadley: I agree. Having an example makes the point better than anything else would

Jeffrey: also assumption that we have to keep popups as the way of doing these things.. I don't know we agree that popups need to stay a critical part of these flows. Some of our anser might be please keep an open mind, maybe getting rid of popups is the right answer

Dan: related to payment flows?

Jeffrey: payment and login of various sorts

Peter: talks about login flows and id as a service providers

Jeffrey: lots of sites find it useful to contract out their authentication

Peter: they use particular mechanisms that rely on third party cookies. There are other mechanisms that don't necessarily require this. Not sure if the use cases are broad enough.

Jeffrey: a bunch of small companies probably really need this to work

Dan: is it necessary to add this new thing which adds a whole bunch of new complexity in the UI, and a new kind of identity that the user needs to be able to parse, in order to satisfy these cases? Or can the cases be satisfied with existing technologies? Is it just trying to streamline something? Or do we really need this witout 3p cookies or we can't do it? The other question is if not FedCM then what other technologies are in the pipeline that could more reasonably implement this user flow? Rather than a new type of partitioned identity.

Peter: is there anybody really working on the SSO type solution? There's also.. I know I've seen various review requests for managing logged in state. I wish .. it's long overdue that browsers have a role to play in user authentication and session management. Almost every website ends up rolling their own or falling back on some third party provider. We have Basic Auth which has bad UX. Client Certs has its own problems. Everybody has to role something else. Why don't we have proper APIs in the browser to begin sessions, detect if the user logged in, do session management/ If we had those we could add the hooks to do third party providers and SSO in a clean way.

Dan: instructive anecdote - I agree with the doom and gloom. On the other hand... I bought cheese, wine and chocolate - all essentials - from websites that supported web payment. I didn't have to log into any of those sites. I used web payment from my browser. I said I want it delivered here. I didn't use apps. Nobody tried to steer me to apps or login. No SSO. That's the future we hsould be pushing people towards. This is how I want to be using the web. It doesn't ask for more than it needs, and it provides chocolate, wine and cheese. All using browsers blocking third party cookies. These capabilities do exist.

Dan: I can log into dev.to with Github credentials, even without 3p cookies, so what's the real problem we're trying to solve here.

Jeffrey: Federated identity is actually a privacy issue; we'd rather people use 1p login.  Someone's going to be able to smuggle identifying info through URLs... 

Peter: that's what SAML does...

Jeffrey: maybe the answer to this API is - we're not gonna block SAML so why do you need these pop-ins?

Jeffrey: I don't think we'll be effective if we just say "don't do this". I think we can say "we're still nervous" - please keep looking for alternatives.

Peter: Someone should be working on solving Okta "well".

Jeffrey: I think this team would say that's what they're working on, that if the UI can be solved, partitioned popins are a good way to handle Okta's use case.

Peter: I worry this isn't specific enough, and there aren't enough hooks for the browser to mitigate it. Rather a narrow focused API to solve the proper use case, that can't be abused for other things.

Dan: Johann might say this _is_ the focused API.

Peter: This isn't though; it's not focused to authentication.

Peter to post:

<blockquote>
Hi @johannhof - We're more concerned with the UI complexity. Specifically, how can we communicate to the end user the nuance of the partitioned identity?  Feels like the spec should give an example of good UI - or indicative UI - especially since this informs the user's decision-making process, for example regarding what permissions to agree to, and this will be a new situation that they may not have encountered before?

It seems like some of these use cases could be solved by a narrow, focused API that is built to solve the specific use case (login flow), rather than by introducing a new technology that also introduces a new kind of partitioned identity, which introduces the potential for user confusion (and abuse).
</blockquote>

### [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman

Jeffrey: I drafted a closing comment in https://github.com/w3ctag/design-reviews-private-brainstorming/issues/34#issuecomment-2546235636. Want Martin to review the bit on Multiformats. Should we be stronger on our polyglot concern?

Tess: It's fine.

Jeffrey: I'd like us to do a finding on how to do extensions, to remove the reason lots of people pick JSON-LD, but can't volunteer to drive it.

Jeffrey: -> Breakout B or Plenary to get Martin's feedback.

### [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

Matthew: We don't have any comments on the brainstorming thread. Don't know if it's a lack of opposition. I asked all the questions I needed and it was fine. Don't see anything from an a11y perspective. Others want to chime in?

Peter: I think everyone else had looked at it and not had any issues. Close as satisfied?

Matthew: okay

### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

Dan: Think we'll leave this to the future TAG.

### Endorse [process PR about Timbl and councils](https://github.com/w3c/process/pull/792)?

Jeffrey: Think we need to tell the AB that the TAG as a whole agreed on a direction.

Dan: Wait to plenary?

Jeffrey: Think we already had the discussion (https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/10-28-minutes.md#adjust-timbls-tag-status), and we said we'd go the direction the vote leaned.

Hadley: Did Tim weigh in?

Yves: Ralph asked, with no answer.

Peter: Should record that the TAG supports #792. #791 is still open. Could do it in the future.

Dan will post to #ab-tag channel.


### Switch [scroll-start-target](https://github.com/w3ctag/design-reviews/issues/1011#issuecomment-2537288349) to satisfied?

Dan: Happy with that.

*no objections*

Jeffrey: I'll do that.

### Schedules for next year

*We agree to not hold calls for the last 2 weeks of the year - but we will start up again on the week of 6-Jan-2025, same schedule that we have been using.*



## Breakout B

Present: Peter, Jeffrey, Martin, Tess

Regrets:


### [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman

Martin's happy with the closing text. Jeffrey had second thoughts about "satisfied", and we closed "with concerns".


### [Improve the run-to-completion principle.](https://github.com/w3ctag/design-principles/pull/536)

[Discussion about whether the comments were handled correctly. General agreement; Martin merges.]

### [Add a section about looking for guidance in other specs.](https://github.com/w3ctag/design-principles/pull/542)

Martin merges.

We might want to remove https://w3ctag.github.io/design-principles/#using-http and put its content into this new section. Jeffrey will send a PR to do that. But there are also some issues asking for Web-specific HTTP guidance, so we might eventually wind up expanding that section instead.

### [CSS advanced attr() function](https://github.com/w3ctag/design-reviews/issues/513) - @hober, @dbaron, @plinss

Tess: Not all the CSS PRs are closed.

Martin: Your general disposition is positive, there are just details?

Tess: Yes.

Martin: I want to use this. It's nontrivial to implement but useful.

Peter: -> pending feedback

Tess: happy to close our review once they've closed their issues.

### [Early Design Review: Allowing First-Party SameSite=None Cookies in Sandboxed Contexts ](https://github.com/w3ctag/design-reviews/issues/1004)

Jeffrey had forgotten that he thought about this in October: 

> SameSite=None remains the most confusing cookie property. The use case seems fine to me, but I'm torn between wanting the sandbox value to say something about the meaning of a frame with this value set, vs saying specifically what it does. Sandbox values have so far said just what the effect is, so it's probably right to continue that policy, as this proposal does. This also seems to require browsing contexts to track more data, since right now they just have an origin, which is set to opaque for most sandboxed frames, and this would require them to save a site and use it for only certain cookie requests. Tentative response:
>> Thanks for sending this to us. We think the use case looks reasonable, but we'd like to make sure that the relevant working groups get a chance to check that the behavior is right and that this doesn't add too much complexity to spec and other-engine infrastructure. In particular, it looks like it might be tricky to save the site so it's reliably only used for including these particular cookies in requests. Please drive w3c/webappsec-csp#664 to a conclusion, and work on a PR for the appropriate sections of HTML.

Martin: Isn't this a self-own on the part of the page, which sandboxed a frame that needs cookie access?

Jeffrey: Kinda. I don't fully understand the use case, and the iframe could always be allow-same-origin, but maybe you want to give it less access.

Martin: I really don't like this whole cookie setup. The argument seems reasonable, but it's all a death by 500 papercuts.

Jeffrey: Both `sandbox` and `SameSite=None` are confusing, so of course we need to combine them.

Martin: I think Jeffrey's draft comment is roughly the right thing to say.

Jeffrey: Maybe we should also say that this whole area is hard to understand and could use a rethink, but we haven't done that, and these proponents aren't really responsible to do it either.

~~~
Thanks for sending this to us. We think the use case looks reasonable, but we'd like to make sure that the relevant working groups get a chance to check that the behavior is right and that this doesn't add too much complexity to spec and other-engine infrastructure. In particular, it looks like it might be tricky to save the site so it's reliably only used for including these particular cookies in requests. Please drive w3c/webappsec-csp#664 to a conclusion, and work on a PR for the appropriate sections of HTML.

We are reminded again that cookies are now at the point that you need a doctorate in that domain to make any sense of them.  The combination with the [iframe sandbox attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#sandbox) really takes it to the next level in terms of web developer hostility.  That's not your fault, but we think that this area of the platform is well overdue for a serious rethink.

~~~

### [[Handwriting] Add Handwriting CSS Value](https://github.com/w3ctag/design-reviews/issues/1018)

Tess: We like early reviews, but this is very early.

Jeffrey: They've had discussions in Pointer Events, so it's not as early as the location of the explainer would imply.

Peter: Initial thought is "why?" 

Jeffrey: Seems like handwriting and panning were getting confused for each other.

Peter: Might be a UA bug. If it takes text, the UA should accept handwriting, and it shouldn't be the author's problem.

Martin: pan-x + handwriting? Is that nonsense?

Jeffrey: Ask them those 2 questions?

Martin: If something is handwriting, is there an expectation that we draw the handwriting? If you want text input, use `<input>`, and let the OS/browser deal with the input.

Tess: But sites do wacky things with `contenteditable`, and I'm tired of yelling at clouds. It's easy in all-too-common shenanigans case to need to say that various regions accept scribbling and others don't. Bad that you end up there because of the compounding of other problems.

Peter: Not excited about supporting the above. Also bad that this proposes to monkeypatch CSS.

Martin: I'm less negative than my initial reaction. People shouldn't do this, but it's not MUST NOT. I don't know enough about touch-action to be able to say.

Tess: Default UA behavior should be good. On a boring HTML page with `<input type=text>` or `<textarea>`, handwriting should Just Work without confusing the page. But in the case where there's a disconnect between the thing that accepts input and the thing the user's manipulating, it seems like you need an escape hatch like this. Like in a synthesizer that just watches finger position.

Peter: Then you'd want a value that prevents handwriting, not a value that enables handwriting.

Tess: Not sure there's a use case for opting in.

Peter: How do you get everything but handwriting, including future stuff.

Martin: Think that's the intent of the `touch-action` attribute anyway. Weird stuff in the MDN page. Can enable panning left but not right. Don't know why you'd want that. Weird restrictions. In most cases, this seems like the dumb thing to do. Think what the explainer says is that if handwriting is enabled, that's what happens. General shape of this proposal isn't terrible.

Tess: Not uniquely ugly; consistent with the rest of `touch-action`'s weirdness.

Martin: Needs to be clearer about how `touch-action` interacts with other things.

Peter: And the UA stylesheet sets `touch-action` on `<input>` and `<textarea>`?

Martin: Lots of mobile UI will open a box that you handwrite into.

Peter: And then you never handwrite into any element.

Martin: I think this is only for pages that really want to capture user input directly.

Peter: Maybe for when the control is big enough to capture handwriting.

Peter: I'd thought Pointer Events was specific to pen-type devices.

Martin: Nope, fingers are included.

Jeffrey: Should we ask them to talk to the CSSWG?

Tess: It's been a point of contention in the past, but yes.


`satisfied` with:
~~~
Thanks for bring it to us.  We've discussed the feature and it seems like -- while this is a niche sort of thing to want to do -- there are cases where this could be useful.

The design appears to be consistent with the design of touch-action.  We do think that it would be better to clarify the interaction of `handwriting` with other actions that are available.  In many cases, pointer devices (like fingers) are unable to distinguish between a writing and panning mode, so having `touch-action: pan-??? handwriting` doesn't make a lot of sense for those common devices.

We also encourage you to consult with the CSS working group on this.
~~~



## Breakout C

Present: Max, Tristan, Dan, Hadley, Matthew, Amy

Regrets: Lea


### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon



### [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

Max: Matthew suggested to update the explainer... 

Dan: let's revisit in the plenary and ask jeffrey to ping elad?

Matthew: we might be able to close it... the main thing about my post: clarifying what I meant by UI changes... don't think we necessarily expected a reply... 

Dan: let's close at the plenary.

### [EPUB 3.3 Recommendation with Candidate Corrections  2024-10-17 > 2024-12-19](https://github.com/w3ctag/design-reviews/issues/1006) - @rhiaro, @hadleybeeman

Hadley: ready to close. Most of the changes aren't architectural, Jeffrey picked up one which was the change came from using wrong definition of whitespace - infra definition instead of xml - so they changed that and Jeffrey filed an issue with whatwg to give them a heads up if they want to clarify the language in infra.

Matthew: APA reviewed and it looks good to them.

Hadley: the point Jeffrey raised - there was confusion and we provided some guidance.

~~~
Thank you for bringing this our way. We've filed a (PR regarding one minor point on white space)[https://github.com/whatwg/infra/pull/649]. However on the whole, we don't think there are any architectural concerns here. Thanks for flying TAG. 
~~~

**we agree to close as satisfied with the above comment**

### [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017)

Dan: we had a discussion a while ago about clipboard access and whether tehre should be any requirement to use the paste command in order for the web app to gain access to the contents of the clipboard. I still feel that is the case. A web app should never have access to the clipboard unless I explicitly tell it I want to paste something from my clipboard. It seemed like.. this issue still has not been resolved.. there are people who feel there are circumstances even without a permission grant that a web app should be able to access clipboard contents. I guess because some applications can access it without user interaction. Which is also frightening.

Amy: what's the use case? why is immediate clipboard sync useful?

Matthew: it can be a convenience... 

Tristan: I use cross-device copy-paste all the time... 

Amy: I'm skimming the user stories and they don't feel like user stories. Also worried about information leak.

Dan: I don't expect that the remote client automatically syncs the contents of my clipboard. What I expect is that I copy something from Mac and go to the Windows environment, press paste, and and then at that point content is pasted. There's an action required. I'm concerned with anything that's polling or event based. I can understand if you've gone through the situation of having installed a remote desktop client but in the web context I'm extremely worried about it because it can provide access to information that you wouldn't expect. It's an attack vector.

Matthew: I see those concerns. You can do the magic cross device copy paste, just make it a pull rather than a push, on a user action. Also concern about things that involve events or polling - implication I'm seeing you can already do it with polling.

Dan: that's exactly where my mind has gone

Amy: It does say "It provides an efficient alternative to polling the clipboard for changes."

Dan: let's discuss async and then decide what to do at the plenary.

### EWP blog post

Dan: in response to people asking about how the ethical web principles are actionable, wanted to restate that. https://www.w3.org/blog/2024/ethical-web-principles-building-a-better-web/


## Plenary Session

Present: Hadley, Amy, Martin, Matthew, Sarven, Dan, Tess, Jeffrey, Peter

Regrets: 


### Breakout Rollup

#### Breakout A



#### Breakout B

#### Breakout C

##### [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

Matthew: I think this is done - no comments on brainstorming thread - 

Martin: you capture another tab and you want to be able to scroll it...  It's cooperative so it's fine.

**matthew to close**


##### [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017)

Dan: *reprises discussion from breakout C*

Amy: there is info in the explainer about privacy levels and also user activation... 

Jeffrey: the fact that several applications like excel and google docs - want to show "you have this data to paste" - they can probably do that without access to the data. It's important that remote desktops be implementable on the web... but they can probably do this and also meet privacy goals...  Also google and apple have been active on the spec...

Hadley: that's good news

Sarven: is there any doucmentation on the same category of things being a threat? As far as I know, clipboard is managed in the RAM. You can always come with a use case... Should there be any room for having any access in the RAM?

Martin: I agree with Dan. Lots of things go across my clipboard, and if arbitrary webistes could access that, it's terrible. there are constraints around the use of hte clipboard: it has to be foregrounded, etc. But I think there is a difficult question about what it means to be an agent, to be your computer. A random website acting as your computer is difficult for me, that it might be ok for this website to do that and not others. And remote desktop apps need that capability. When we were talking about access to ubikeys and local passkeys, the remote computer is now wanting to access local computer things to act as your computer and I'm not comfortalbe with that. Just saying "that's ok, this is an important use case" hides the difficulty here. Sarven's point about accessing RAM is putting a sharp point on it. I think no website should have that capability.

Dan:  It feels like that capability, like ubikeys and access to local drives etc, would/could be appropriate if you've installed and given permission to a complete client environment. But it may be that it shouldn't be something the web should do. Maybe it's too powerful for the web.

When it comes to pasting, and access to the clipboard, I still don't see... it doesn't degrade the experience that much to have to wait for the user to press paste before the contents of the clipboard are pasted into the other environment. It's not like you're denying access, just making sure the user really intends to transfer that thing to the other side. Otherwise it could be passwords, urls, any kind of ino in your clipboard.

jeffrey: The thing the user does to tell a site they want to paste may not be ctrl+v, it may be a button. We could use a user gesture, but we can't be sure the user did it all... Also, there are persistent differences between UAs on this question. Chrome and chromium browsers are not going to stop chasing remote desktop as a use case, and firefox and safari and not going to pursue the use case in the same way. So the design question: how to make an api that doesn't create a bad user experience across browsers? I think the clipboard API has been designed successfully. The read event ... If we arrange it so the same code works in all places and degrades gracefully, we will have succeeded. Might be able to say "do this only in IWAs". I don't think chromium will accept "just don't do it"

Torgo: Thinking through the UX, the user might still have access to a paste menu option. It may be that the remote desktop environment has to lead the user through a permission request experience in order to get them to request that permission.

Jeffrey: that permission is what some browsers don't think is a good idea.

torgo: This is why I installed hte clear clipboard thing on MacOS to clear my clipboard regularly. I don't want the text in my clipboard to be siphoned off for other use cases. I don't agree that the current API has been designed well. We are lowering the bar re keeping users safe on the web.

Jeffrey: They present 2 use cases in their explainer. Pressing paste in a remote app doesn't always work, which I think is a bug in the system and not a web issue. 2: they want to know the types of data in the clipboard. I think that's much safer to expose than the data.

I suspect mozilla and safari will be happy with that. probably still worth gating behind a permission, but doesn't seem dangerous like the content seems dangerous.

Tess: interesting weird custom types could be fingerprinting info. But if it's limited to ... distinct from arbirary media points -- not as bad.

Not obvious to the user that granting permission to occasionally paste means this web app will learn that I have photoshop installed on this computer. Or whatever domain specific software I have installed. 

Torgo: probably less directly harmful, but there might be some harms just knowing the types. 

Tess: domain specific application with a proprietary format

*Matthew: For background info, the file-type fingerprinting issue came up earlier in the year with respect to [Delayed Clipboard Rendering](https://github.com/w3ctag/design-reviews/issues/925)*

Martin: You can send messages across domains, since it's easy to put content on the clipboard. It's another channel that shouldn't exist. 

Torgo: I don't know if we'll resolve this here

Martin:  "Chromium wants it, therefore we need to accept that, no matter the moral value" -- I'm tired of this. 

Torgo: I don't know that I agree with that wording, but in some cases we have pushed back hard on APIs that have been presented to us for design review such as the managed device API... we said we can't stop anyone from writing something in their own software, but this shouldn't be part of the web platform. 

"XYZ company, you have business requirements to do a particular thing, but that doesn't mean we have to put it in the web platform. You can deal with it iwith your own business partners." It was intended for IT people to manage and monitor what the users in their enterprise were doing, and it's not something we need to do on the web.

*the tension between not reviewing things that we think are not a good idea and trying to push back on things to make a difference where we can - harm reduction*

...Let's defer this to next year. No consensus now. 

Jeffrey: I can draft a comment for the private-discussion thread.


#### Societal Impacts bonus meeting ✨

https://github.com/w3ctag/societal-impact-questionnaire

Torgo: making a difference... harm avoidance... we had a meeting earlier. As we discussed in the call, this doc is -- we haven't done a lot in the past year. Now that we have the Ethical Web Principles as a statement, it's time to start doing more work on this. Got some good feedback from folks. Tristan is interested in becoming an editor, Sarven might be co-editor too. Amy has been the editor, but it needs new editor(s) as they leave. Helpful to relate this to other threads like the sustainability work we're doing. 

We merged a PR on surveillance

Amy: Yes, that was the summary

Torgo: let's take this forward in the new year

Sarven: unofficially, I'm happy to contribute to this. I'd like to discuss processes re who puts effort in which direction, what needs attention, also what I'm interested in. So I can have an impact while i'm with you.

Torgo: we had a lot of discussions in our last face-to-face in Edinburgh about how we work, what the right ratio is between the design reviews and other technical-direction type things. Consensus was more of our time on techincal direction and less on design reviews. We need to figure out how to do that. We also talked about TAG associates to bring in other people to help. We need to hammer out this stuff in the new year.

Hadley: also: feel free to tell us if "how we do things" doesn't make sense or you see how we could do it better. We undoubtedly could do it better, and your thoughts would be great.

### March f2f

Tess: i agreed to ECMA exacom on the same dates -- I'd love to do both. We usually do a half day planning and three days of f2f. If we somehow did the planning before hand, I could do two full days of TAG (3-4th) and two days of ECMA, that would work.

Torgo: Tristan said he'd try to find a room for us in Paris.

Tess: if that falls through, I could try.

Torgo: It's been a bit of inflation... we had a 3 day f2f, and then added a half day to organise our agenda. But we could do the agenda in a virtual session in previous week and see how we think it worked.


### Welcome new TAG members

* [Sarven](https://csarven.ca/#i) :wave:

### Appointing some Associates for January?

### Finding progress

* [User agents finding draft](https://w3ctag.github.io/user-agents/)

Jeffrey: this is published to the repo. Please file bugs. 

* [Commons](https://lists.w3.org/Archives/Member/tag/2024Dec/0008.html)

Jeffrey: I've sent it people. Haven't heard about having a pre-IASC workshop  yet.
