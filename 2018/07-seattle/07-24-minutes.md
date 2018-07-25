# W3C TAG face-to-face in Seattle
## Day 1

Present: Kenneth, Sangwhan, Hadley, Travis, Peter, David, Daniel, Yves, Lukasz (remote)

Scribe (AM): David

Scribe (PM): Kenneth, Dan


### Agenda setting

Dan: (going through fixed points in schedule.)  Do we have a time for Accessibility Object Model?

Layered APIs

Badging Proposal

Adaptive Icons

Gamepad API and WebXR

Plan Layered API discussion for 10am Wednesday, with Ojan calling in.

Peter: We have a lot of HTML issues.

Yves: Can we try to close issue 76 when Mike West is around?

Dan: HTML issues this morning?

### HTML Issues

[HTML Issues](https://github.com/w3ctag/design-reviews/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aopen++%22HTML+General+Review%22)

#### [HTML General Review: HTML Document and Elements](https://github.com/w3ctag/design-reviews/issues/242)

Dan: Travis, you're already assigned.

Adding various others.

#### [HTML General Review: Structured Serialize/Deserialize](https://github.com/w3ctag/design-reviews/issues/243)

Travis: This is about structured clone.

Kenneth:  People need this, but also don't understand what it is and isn't.

Alex: I have a big issue about it not being extensible in any meaningful way.  Can't plug in alternative algorithms for particular objects / graph types.  Also totally synchronous.

Dan: Stuff we could put into some notes for recommendations.

Kenneth: Would be nice to start with actual use cases.

(discussion about use as deep clone)

#### [HTML General Review: Custom Elements](https://github.com/w3ctag/design-reviews/issues/244)

...
Alex: There's a larger question about reservation of attribute names, since they're global.  But nobody actually implements that restriction.


#### [HTML General Review: HTML Linking](https://github.com/w3ctag/design-reviews/issues/245)

Travis: one major issue is the `ping` attribute on `<a>`

Breakout: Hadley, David, Peter, Dan

David: Gecko removed support for xml base that could change because we didn't want dynamic changes to base URLs. 

David: Does this have tests? - 2.4.3 when a document's base URL ...  Seems like it attempts to describe browser behaviour.

Peter: URLs in CSS, multiple base elements...

David: I could write some tests...

Dan: that's not our role... TAG recommendatioons?

Peter: deprecate the base element?

Hadley: how do we square dynamic changes with the idea that URLs aren't supposed to be change. E.g. if you use a URL as an identifier you want it to be the same URLs

David: nobody likes dynamic changes to base.   [use cases are unclear]  I don't think it happens much.

Dan: so we could suggest this ought to be depercated?  That's in scope.

Peter: this is huge hole for the platform. it doesn't work consistently or predictably. Nobody wants to take the time to fix it. Curious what the use of the base element even is...

David: I regularly use the base element when simplifying test cases...  But other ways exist to simulate that.

Peter: I'd like to see what the use is... 

Hadley: should we add to death panel?

Peter: if you say "you can have a base element but you can't change its source" there could be ways around it...

David: the web platform tests have 19 tests - 19 pass in firefox but only 1 pass in chrome, edge and safari. The test is called dynamic changes to base URLs.

Dan: [makes note in issue]

Dan: Anything else we can cross off?

Peter: not much more to do on preload.

discussion on rel=no_referer - Peter: means don't send a referer header if you click on this link

Dan: anything to comment on for 4.6	html/semantics/links ?

[consensus no]

Hadley: normative reference to microformats wiki - 4....

David: at least it says where the registry is and how to update it... that said there are quite a few registrations on here... 

Hadley: what is the process for pulling stuff out of this registry?

Dan: PING element: https://github.com/w3c/html/issues/1456

David: currently disabled in firefox (due to community pushback). 

David: argument is that people will do it anyway by running you through a redirector. If you hover over the link it shows you to the right thing - and then they use javascript in the click event to change it to go to a redirector...

Peter: could be done with service worker.  People will get do stuff to get this behavior anyway.

David: and it's faster with the ping than with the redirector.

Hadley: you can control some of that behaviour by blocking by domain etc... This gives away the user's power. What is the use case that benefits the user?

Peter: the benefit to the user - links work faster but also the browser can have a setting that turns that off, or if in private mode it doesn't send those pings...  

David: google search results appear to use ping in chrome but not firefox.

David: they want something reliable for if you've clicked it

Hadley: I have a fundamental problem with that - that sites should have total info for everything you're doing.

David: they [search results] want to know what you click on...

Hadley: as the user i don't think it's my responsibility to give it to you.

Peter: counter argument - everuone who runs a site that runs ads or does e-commerce wants this analytic data. Default answer is to put ggoogle analytitics in your page. If we have better tools then you can collect the analytics yourself without having to rely on a 3rd party.

Hadley: slightly less bad but still bad.  I am concerned that our web is too skewerd towards publishers/develoeprs/websites.

Dan: what can we do to mitigate against this?

Hadley: most users don't think this is a choice. at a bare minimum some transparency that implementing this option is optional and increases the surveillance of users is an important stake in the ground. 

Peter: if you want to protect the privacy you have to pretend you have this feature - 

Dan: so it would have to mimic feature detection

David: for permission prompts we - not sure we can do that here ... 

[...discussion on who cares about privacy...]

Hadley: user agents haven't prioritized...

Dan: what specific recommendation shsould we make into the spec to sign-post the privacy issues?

[the spec for the `ping` attribute](https://html.spec.whatwg.org/multipage/links.html#hyperlink-auditing) says:
> 2. Optionally, return. (For example, the user agent might wish to ignore any or all ping URLs in accordance with the user's expressed preferences.)

Peter: what's missing here - I don't see any mention of CSP.  The PING URL should be protected by CSP of the page that contains the link. .. malicious injection of PING atrtibutes

Hadley: ...inform the user about where they're going...

Dan: I am concerned that this whole document (https://html.spec.whatwg.org/multipage/links.html#hyperlink-auditing) doesn't include the word "privacy".  Can we agree that TAG should feed back that this section should inlcuudel sttronger privacy considerations and risks including behaviuour recommendations in private browsing mode.

Hadley: private browsing mode is a part of it but it's missing the bigger point...

Peter: iti feel it's shifting control back to the user.

Hadley: this also legitimizes it.

Peter: this along the same lines as having an ad element - gives the browser theoretically far more control.

Hadley: part of what bugs me here is the that the implication on is that this is it's supposed to work.

**Action**: Hadley to write up something on `ping` attribute specifically

Hadley: other than that I'm not aware of other link issues.

Peter: Is there a way for CSP policies to integrate with `ping`?

#### [HTML General Review: HTML Styling](https://github.com/w3ctag/design-reviews/issues/246)

Dan: what actually needs to be talked about?

David: `innerText` is pretty awful, but we're stuck with it.

Alex: `<style>` raises question about load time attributes `sync` and `defer`; magical and not under developer control.

Breakout: Hadley, David, Peter, Dan

David: `innerText` requires styling - and it's important pfor performance on the web.   For `innerText` you can define you only need style on the descendents.

Peter: a lot of people are using this.

David: yes.

Dan: we should not worry about innerText too much

Dan: the `<style>` element

David: people have complaints about loading of style sheets.  Media restricted style sheets.  Like style sheets with a media query.  uShould you load the style sheet?   Style loading isn't sync.

Peter: it blocks rendering

David: mostly but not completely

Dan: is there something we can feed back agbout this?

David: people want a way to link to media specific style sheets and have the browser not load them if they are not needed.  Users resizing a window is a pretty rare operation... so lower priority.

Dan: is there an open issue somewhere on this?

David: `<script>` has `async` and `defer` does `<style>`/`<link>` have thes things? [no]  Scr

Dan: if there is no related whwatwg issue should we create one?

David: [researching - emailing Henri Sivonen]


#### [HTML General Review: HTML Lists](https://github.com/w3ctag/design-reviews/issues/247)

David: maybe not that much here

sense that we don't need a breakout for this

David: I'd love to be able to continue lists later.

Alex: styling of marker, isn't it shadow DOM?

#### [HTML General Review: HTML Ruby](https://github.com/w3ctag/design-reviews/issues/248)

David & Sangwhan: Multiple algorithms.

Sangwhan: Hixie's algorithm in one spec and Berjon's in the other spec.

David: worth seeing if there's stuff we can push towards converging

Breakout: Hadley, David, Peter, Dan, Sangwhan

David: the W3C and WHATWG versions are different right now. W3C version has the `rb` and `rt` elements which the WHATWG version does not. 

Dan: what are the implementation sdoing?

David: Gecko implements all of those pieces.

Sahgwhan: ththalso theres the rb  rt

Hadley: html issue 1424 - linked to from our issue and chaals satitiying we should make this ast risk and fantasai and ishida saying please don't.

Dan: are the bits neot in the whatwg verison i
mportant?

Sangwhan: I would say so. there have been issues raised by the community on authoring ruby content... The part that I woudl be concerned about : this is both defining a layout mechanism and a data mmodel and I'm not sure long term whether it should be kept this way

David: there is a CSS ruby spec as well... Potentially 4 models 

Peter: several TPACs ago Robin Berjon and Elika sat down and figured out how to do this right.

Sangwhan: CSS ruby has progresse  d, HTML ruby is spetuck

Dan: should we focus on html ruby

David: yes but models need to agree with eachother. We need to get the right people in the room to discuss this. 

Hadley: are we sure it's broken?

Sangwhan: yes. Crossbrowser interop is broken.

Sangwhan: hixie version (current WHATWG spec) according to the CJK community is unusable.

David: some things japanese community think may not be needed that are currently in the [css] spec 

Sangwhan: Three versions: w3c html ruby, whatwg ruby, css ruby

Sangwhan: i would like to organise a breakout at TPAC to figure this out.  

Sangwhan: there is a publishing summit in tokyo - if enough people are coming I could do a breakout there.

**Action** Sangwhan to organise pmultiple breakouts.

#### [HTML General Review: HTML Images](https://github.com/w3ctag/design-reviews/issues/249)

Yves: external spec for async loading.

Sangwhan: `decode` attribute.  Also decode API.  Loading algorithm on W3C side has some issues.

Dan: better to focus on WHATWG spec.

Alex: lots of feelings about decoding APIs, should work with streams, etc.

Breakout: Hadley, David, Peter, Dan, Sangwhan

Sangwhan: i am the sole spokesperson for Alex Russell

Sangwhan: ENo APIs on the platform for decoding/encoding bytebuffers or streams. Would be useful to get rasters and other objects out of raw data... both decoding and encoding... would be  nice to have.

Dan: is there an open issue somewhere on this already?

David: i don't think so - it probably shouldn't go straight into HTML - it should probably be developed

Sangwhan: it should be exposed to more than just the document context - should be available to a worker.

David: should there be general APIs for loading from a stream into some set of things?  Are there many types of those things?

Sangwhan: fetch has toJSON, etc.

David: but that seems oddly specific to fetch, rather than general to streams

**ACTION** Sangwhan to ping Domenic about it.

#### [HTML General Review: Browsing Contexts and Security](https://github.com/w3ctag/design-reviews/issues/250)

David: at some point in the past we had a discussion about the number of allow/deny mechanisms for iframes

Travis: went in to feature-policy

Breakout: Hadley, David, Peter, Dan, (Travis)



#### [HTML General Review: HTML Media](https://github.com/w3ctag/design-reviews/issues/251)

Sangwhan: are MSE and EME integrated properly into the loading algorithm -- I don't believe it is.  And are there things that work that aren't referenced in the spec?

Alex: same question about codecs, encoders/decoders, as for images.

#### [HTML General Review: HTML Tables](https://github.com/w3ctag/design-reviews/issues/252)

David: I don't expect a lot of enthusiasm about adding features to tables.

Alex: Can't take a CSV file and pull it into a table without lots of JS?  Should talk about where data comes from -- why can we load/decode audio/video but not data.

#### [HTML General Review: HTML Forms](https://github.com/w3ctag/design-reviews/issues/253)

Alex: many opinions about forms

Kenneth: important for custom components to become submittable

Alex: why is the vocabulary that form elements speak so impoverished?

Travis: meaning all name=value pairs?

Alex: yes, e.g., no way to say form is representing an address

#### [HTML General Review: HTML Input](https://github.com/w3ctag/design-reviews/issues/254)

Sangwhan: validation built into browsers is often very restriction; people often building their own, e.g.,  for `<input type=email>` only taking ASCII email addresses.

#### [HTML General Review: HTML Option Lists](https://github.com/w3ctag/design-reviews/issues/255)

Alex: Why can't I feed option lists with data?

#### [HTML General Review: HTML User Interaction](https://github.com/w3ctag/design-reviews/issues/256)

Kenneth & Travis: something about `summary`/`details` and shadow DOM

#### [HTML General Review: HTML Focus](https://github.com/w3ctag/design-reviews/issues/257)

Peter: we have a separate issue on Spatial Navigation (spatnav).

Alex: focus and activation should be hierarchical, you should be able to add your own actions, etc.

David: I remember a long discussion between CSS and a11y at a TPAC maybe 6-10 years ago... (oh, it was about `tabindex`/`nav-index` in November 2011, see [email 1](https://lists.w3.org/Archives/Public/wai-xtech/2011Nov/0034.html) and [email 2](https://lists.w3.org/Archives/Public/wai-xtech/2011Nov/0035.html))

#### [HTML General Review: HTML Scripting](https://github.com/w3ctag/design-reviews/issues/258)

Dan: link to other issues on modules, etc.?

Dan: keep low priority for now?

#### [HTML General Review: HTML Templates](https://github.com/w3ctag/design-reviews/issues/259)

Dan: Seems like priority should be review of new work that's coming rather than what's already there.

Dan: Take to breakout and list that stuff.

#### [HTML General Review: HTML Drawing](https://github.com/w3ctag/design-reviews/issues/260)

David: most but not all of 2d context is being reused by CSS Paint API in a way that it doesn't have to be backed by a bitmap but could be backed my a display list.

Sangwhan: My interest was encoding and decoding.

Travis: Also WebXR commit proposal.

Alex: I'm worried about commit.  synchronous.

Travis: I like it better than `ImageBitmap`.

#### [HTML General Review: Microdata](https://github.com/w3ctag/design-reviews/issues/261)

Hadley: largely search engine consumers rather than browser consumers.

Alex: people break their microdata since it's not related to the UI.

#### [HTML General Review: Navigation and Browsing History](https://github.com/w3ctag/design-reviews/issues/262)

assigned Travis

#### [HTML General Review: App Cache](https://github.com/w3ctag/design-reviews/issues/263)

Dan: isn't it deprecated?

Alex: is it *marked* deprecated?

Yves: I think there was a discussion about deprecating it in the W3C version... not sure if it was done or not.

Sangwhan: was not

Sangwhan: discussion could be around the process of deprecating and obsoleting features


### WHATWG and TAG

Jeff: opportunity to have a single workstream for HTML.  Goal of zero normative differences.  How to do conflict resolution?  WHATWG process has conflict resolution in its process.  W3C has process of raising formal objections to the director; we hope this option is rarely used.  Want to ensure there's dialogue before it gets to the director.  Want to make our highest technical body (the TAG) available to look at the issue and try to get to consensus.  TAG agreeing with editor might discourage objector from continuing; TAG agreeing with objector might make editors reconsider.  Want to get TAG's view of this role.

David: I think the editors are open to listening to technical opinions from the TAG and being convinced.

Alex: Issue of representation.

Dan: Future questions of positions on TAG elected by web developer community.

Hadley: I'm worried about the number of differences that might go through this process.

Jeff: Better to have the discussion than have separate specs.  Also nothing prevents either organization from creating separate extension specifications.

Dan: I worry this sets the TAG up to be a place where people have disagreements.  But this seems like a better position than other cases where we tried to mediate but we didn't have standing with the parties to the dispute.  Would like the TAG to sign off on the text referring to us in the agreement.  And I'd like the wording about the TAG's role to be more precise about what the TAG does and when.

Jeff: The less the TAG is involved, the more likely these disputes are to go to the director.


### HTML Issues, continued

#### [HTML General Review: HTML Utilities](https://github.com/w3ctag/design-reviews/issues/264)

David: Share Target and Share has some relationship to protocol handlers.

Alex: the overlap between the two features is that people have been trying to use protocol handlers to share data to other apps (similar to iOS native apps). Shared Target is much more scoped.

Kenneth: atob could also be in KSJS

#### [HTML General Review: HTML Parsing](https://github.com/w3ctag/design-reviews/issues/265)

Travis: One of the most polished parts of HTML :-)

Travis: is there a feature policy to turn off document.write?

Daniel: document.write is considered pretty awful? Should we make recommendation? Should we have a breakout?

Yves+Alex: no - not much we can do to change this, let's close it.

#### [HTML General Review: HTML Timers and Timeslicing](https://github.com/w3ctag/design-reviews/issues/266)

Kenneth: there are multiple rAF in workers, XR, window.

David: Has relationship to other sparts, like workers, VR etc

Daniel: Are these already covered in other issues? Shall we close? or is it worthwhile having further discussions?

Daniel: Lets focus on the new issues and not what is in HTML spec - or at least paste the other issues into this one. Closing it.

#### [HTML General Review: Server-Sent Events](https://github.com/w3ctag/design-reviews/issues/267)

Peter: Should be closer to fetch, send credentials etc.

#### [HTML General Review: Web Sockets](https://github.com/w3ctag/design-reviews/issues/268)

Yves: In general most specs should move to streams

#### [HTML General Review: Cross-Document Messaging](https://github.com/w3ctag/design-reviews/issues/269)

Yves: welcome to flat document society j/k :-)

Alex: We need an onclose on MessageBoards - needing to poll is really bad.

(discussion between Alex and Travis)

#### [HTML General Review: Web Workers](https://github.com/w3ctag/design-reviews/issues/270)

Travis: I have a history with those workers, so signing up :-)

Travis: there were interest early on at MSFT in spinning up the workers infra without using the web platform

Daniel: Any useful info we can provide?

Travis: I expect it to be mostly okay...

MINUTES



#### [HTML General Review: Web Storage](https://github.com/w3ctag/design-reviews/issues/271)

Kenneth: not async, so Google is proposing a layered API called async local storage, similar to localForage

Kenneth: We were asked to review the async local storage API

Kenneth: related to layered APIs, indexedDB etc. Before layered APIsww, no browser wanted to add something like that because it could be done on top of indexedDB . This seesmms to be changing with layered apis

#### [HTML General Review: XML Infrastructure](https://github.com/w3ctag/design-reviews/issues/272)

Travis: Domenic reached out to me a couple of time ago, about DOM parsing/serialization spec, to discuss to bring it back into HTML spec which p restarted the XML discussion - how much belong there.

Breakout: Hadley, David, Peter, Dan



#### [HTML General Review: HTML Obsolete Features](https://github.com/w3ctag/design-reviews/issues/273)

Kenneth: Should we give comments when these are actual obsolete?

Daniel: if they are obsolete, they are obsolete - my proposal is that we close this up - we should be looking forward and not back.

#### [HTML General Review: IANA Registries](https://github.com/w3ctag/design-reviews/issues/274)

Travis: No tests?

Kenneth: how do you test registries?

Peter+Alex: General discussion about how registries should be maintained

David: This is about HTML registering itself in IANA (mime types etc), not the HTML spec creating registries.

Daniel: This is a broader topic than this issue, can we close?

## Group 2:

#### [HTML General Review: Web Workers](https://github.com/w3ctag/design-reviews/issues/270)

Travis: Workers still need to yields due to events

Alex: Bad for anything in there that needs to handle user input

Kenneth: Seems to be usability issue as people are writing libraries about this, in a grand central dispatch way, like Tasklets, Comlink etc.

https://github.com/GoogleChromeLabs/comlink

https://github.com/GoogleChromeLabs/tasklets

Sangwhan: DOM access from workers is requested a lot

Alex: The problem is getting access to DOM nodes, finding and referencing them cheaply, I suggested to our teams that everyone should just adopt IEs unique id feature

Travis: breaks across multiple page loads, elements get different ids... first touched element got id 1 etc...

Travis: Blocks proposal: https://github.com/domenic/proposal-blocks

Kenneth: So could this be used for setTimeout etc? I get that devs might assume that.

Travis: something designed around being run once would be quite useful. No need for message passing

Kenneth: Similar to cloud functions, serverless.

Alex: What do we expect to add here? Lots of recent additions, worklet, module workers

Alex: Sub-workers - ability to run worker from worker

Travis: Been in Edge since the beginning.

Alex+Travis: importScripts discussion. Async only works in non module workers. Special in SW in Chrome, you should import in top to expect reliable behavior. Like after installed you might be offline.

Discussion around how to find out whether you are a classic script or module

Kenneth: try/catch importScript would work, and other side-effects

#### [HTML General Review: Cross-Document Messaging](https://github.com/w3ctag/design-reviews/issues/269)



















