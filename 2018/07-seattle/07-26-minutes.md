# W3C TAG face-to-face in Seattle
## Day 3

Present: Alex, Kenneth, Sangwhan, Hadley, Travis, Peter, David, Daniel, Yves, Ralph (Morning)

Guests: Mike West for security discussions, Alice Boxhall for AOM discussion

Scribe (AM): Travis

Scribe (PM): Sangwhan

## Review Obsolete Spec Requests ('so called "death panel"')

(Brief discussion about the specific Process requirements)

Looked at [Widgets](https://github.com/w3ctag/obsoletion/issues/3)

Agreed to Obsolete.

Looked at [HTML](https://github.com/w3ctag/obsoletion/issues/1)

Agreed to Obsolete

## Resume Spec Reviews (HTML Edition)

#### [HTML General Review: Browsing Contexts and Security](https://github.com/w3ctag/design-reviews/issues/250)

David: at some point in the past we had a discussion about the number of allow/deny mechanisms for iframes

Travis: went in to feature-policy

Breakout: Hadley, David, Peter, Dan, (Travis)

David: This is pretty large

Peter: There is the "portals" proposal which is related to this.

Dan: let's punt this to when we have Mike West with us

#### [HTML General Review: HTML Media](https://github.com/w3ctag/design-reviews/issues/251)

Sangwhan: are MSE and EME integrated properly into the loading algorithm -- I don't believe it is.  And are there things that work that aren't referenced in the spec?

Alex: same question about codecs, encoders/decoders, as for images.



#### [HTML General Review: HTML Tables](https://github.com/w3ctag/design-reviews/issues/252)

David: I don't expect a lot of enthusiasm about adding features to tables.

Alex: Can't take a CSV file and pull it into a table without lots of JS?  Should talk about where data comes from -- why can we load/decode audio/video but not data.

Break-out: David, Peter, Hadley, Dan

Dan: Alex talked about populating a table with a CSV...  As one example... 

Hadley: there is some good practice for how to display CSVs in HTML from CSV on the Web: 
https://www.w3.org/TR/tabular-data-primer/#html-display

Dan: I think Alex is talking about extending tables .. 

David: a bunch of these things you could implement in javascript - i wouldn't want to add things that people hadn't done before in JS and proved to be useful.

Dan: Is there some work we could do to determine what cool stuff has been build around tables - examples of common usage patterns of what people have built in javascript?

Peter: alex's point was you should be able to do this without downloading 100k of javascript - maybe then it should be a candidate for the standard library.

Dan: we should be recommending some course of action here - and it's up to the community to determine if it should go into html evolution or into a (still hypothetical) standard library...

Hadley: easiest way might be to ask the working groups - WebPlatform and CSS - for what theur long-term vision is and what work is going on already.

Hadley: if there is stuff on our to-do lists then that's one scenario but it doesn't sound like there is. Feels like this is strraying into areas of design. Tables seem sufficient for what I want to do.

Ralph: dragging and dropping a table from your fav spreadsheet into an html editor - are there things the spec needs to have in it to facilitate that?

Hadley: related to Alex's use cases.

Ralph: rich text... a whole lot of implementation work.... any dependencies in the html spec itself?

Hadley: if we're talking about rich text (formatting) then we have what we need for that. It's macros, vb, etc... that's going's going to be handled differently.

Ralph: the objective would not be to create a live spreadhseet in html - but to [reflect tabular data.]

Dan: we can get further feedback from Alex, but the one concrete case that has been proposed is CSV import. 

Peter: the headers attribute on table cells is new to me. Is anyone implementing that?

David: I don't know... It might be useful for accessibility tools.  I suspect this was in html4.  

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

Break-out: Dan, David, Peter, Hadley

David: Datalist ...  [looks at implementation.... confirms in gecko]

David: you can have  an input that points to a data list

[reviewing the spec]

Dan: any recommendation we should make regarding datalist? Should it be extensible? 

Hadley: the first things that comes to mind - discussions abotout find-in-page vs find on the server...  a parallel?
?
?

Dan: is this a feature that many people are using or is everyone building hteitheir own UI widgets to do this?

David: this is not very extensible... so prople probably building their own things...

Hadley: can't think of things where you wouldn't want a drop-down... e.g. post-codes in the UK.  For smaller sets of options... there might be situatis where it's useful. 

Dan: Airport picker in travel...

Hadley: that's a good use cases for this...

Dan: could we recommend that this be extensible.

David: yes.. 

Peter: the mechanism where this hooks into an input element doesn't have an API or explanation. For epople whi ao are building their own custom controls it would be nice if they could reuse this machinery.

Peter: in the case of datalist it could go both ways... (An input could call a function to get possible autocompletions for a current input.)

Dan: Action... ?

Hadley: will the spec authors pay attention?


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

Break-out: Dan, David, Peter, Hadley

Hadley: as we talked about - work on microdata getting eclipsed wby json-ld. but still a lot of microdata out there.  ... the w3c spec has been brought up to date with reality ... Not sure about the state of the whatwg spec....

Dan: question is: what about extensibility in the e-w-m sense? API?   Does microdata only make sense when it's scraped /crawled?

Hadley: yes it only makes sense when crawled.  schema.org is a finite set of use cases... NCan't see the extsnibility argument for changing web microdata in the web ccpage.

Peter: microdata could be in the browser, informing the UA. Having it dynamically generated there makes sense...

Hadley: how is that dynamic generaiton different to ...

Dan: any other kind of DOM manipulation...

Peter: it's not...

Hadley: it feels like schema.org helps to make things like addresses / phone numbers / etc... readable...

Peter: sometimes we don't have the right tooight tooight tools to mmake semantic data ...

Hadley: there are times when from a design perspective it's nice but it makes it difficult for people to understand.

Peter: in the platonic ideal you smake data sematic but lentnteay-out is separate. Microdata is trying to bridge that gap but it shou be beld be an indicator of a gap.

Hadley: it should make it easier for web developers to do the right thing.



#### [HTML General Review: Navigation and Browsing History](https://github.com/w3ctag/design-reviews/issues/262)

assigned Travis

#### [HTML General Review: App Cache](https://github.com/w3ctag/design-reviews/issues/263)

Dan: isn't it deprecated?

Alex: is it *marked* deprecated?

Yves: I think there was a discussion about deprecating it in the W3C version... not sure if it was done or not.

Sangwhan: was not

Sangwhan: discussion could be around the process of deprecating and obsoleting features

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


Daniel: Are these already covered in other issues? Shall we close? or is it worthwhile having further discussions?

Daniel: Lets focus on the new issues and not what is in HTML spec - or at least paste the other issues into this one. Closing it.

#### [HTML General Review: Server-Sent Events](https://github.com/w3ctag/design-reviews/issues/267)

Peter: Should be closer to fetch, send credentials etc.

#### [HTML General Review: Web Sockets](https://github.com/w3ctag/design-reviews/issues/268)

Yves: In general most specs should move to streams

Reviewed the spec, and aspects of Fetch that relate to Web Sockets (and the Streams standard to freshen our memory on backpressure).

Adam Rice had left some previous comments which we fully supported.


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

# Mike West Discussion

### Mike West Discussion: Deprecating non-secure cookie delivery (239)

Mike: would love to give us more detail. HAve you read the doc? Cookies over non-secure connectsisisiions are very bad. Several proposals for dropping cookies for over HTTP.

1. Look at cookie, store creation date.
2. When cookie is updated, if it gegegegegets the same value, we persist.
3. (If it has the same value its dangerous). iiIf you send the same value over and over is a pretty easily detectable signal to attackers.

Ratchet down use of the same-value set cookies. Starting for long-lived cookies (>1 years of no change), then drop them, start bringing this down. WThe action is that the cookie is dropped ffif it meets candidate.

Adverstising ID is one of the key bad players. Broad network inspection can correlatesily. .

Only has an effect if the cookie is sent over HTTP. If it's going over HTTPS, you're OK. Same for Secure cookies, HSTS. preload.

PPrinciple: "persistence is a power feature" and should be moved to secure context. This plan does that incrementally.

Alex: Is this mostly about images, sent as pings, or from documents. Where do you see them most?

Mike: tracking pixels from advertis, but also scripts, iframes, etc., content pulled into 1st party sites. MNN

Being conservative because I expect "freak-outs", so taking it easy at first.

(TAG tends to condone more agressive stance.)

Other approach: mark every cookie sent over HTTP as a session cookie. 

Lukasz: Why not further shame websites, by using additional mark in the URL bar?

Mike: Not sure we can do more in the URL bar.

1160368 (Mozilla bug). N. N. Note that it broke stuff.

Lukasz: What's the final destination?

Mike: No cookies over HTTP ever. EI expect it will take some time.

Dan: Hmmm. One point remdinds me of DNT...? On being more agressive.

Mike: If the lifetime is a year, seems useful to persist the user's opt-out.
 If the lifetime is a day, it makes less sense.

Alex: Seems good if this: Seems good if this incentivises advertisers to move to HTTPS. Mike what have you heard?

Mike: My sources say, the ones that could easily move have done so, the others are having trouble.

Alex: What do you want to do?

Mike: Want to get progress, but from TAG on actions, but also from implementors as well (we want to deploy a change to cookies that is interoperable).

Travis: +1, will need to get additional views. (Mike suggests EricLaw)

Mike: what would "more agressive options" look like?

eAlex: Kinda looking at you  , Mike.

Mike: Various knobs: Number of cookies a site can have. (Chrome using origin, higher limit; Firefox based on registered name, lower limit.)

Hadley: What's the market impact? How much would users notice - how much would they be logged into things not over HTTPS?

Mike: depends on the market, different in different global locations. Rising in Asia, not as high as US/Europe yet. If customers spend most of their time on Facebook/Twitter, you're on HTTPS a lot. Other (e.g., older forums) have likely not migrated yet. Browser branding is helping move sites.

Chrome Security team strategy putting pressure on the TLDs, who in turn put pressure on 

Travis: is there an upper-limit on cookie expiration?  

Mike: 

David: FF limit increased from 150 to 180. In 2016, Twitter was setting per-tweet cookies, which ended up purging the login cookie (which wasn't having it's date refreshed on set to same value). Interesting potential. gotchas.

Mike: have some bad ideas around cookie replacement, but not ready to bring them forward yet.

### Mike West Discussion: Sec-metadata

Mike: idea: we should send the server more data to help it make good security decisions.

 Problem: possible to make valid-looking requests but aren't. E.g., CSRF. Cross-site search: can trick users into making a search request whose response payloads can be analyzed by size.

Proposal takes three fields exposed through fetch and gives them to the server. Adds 1 more field to tell how the navigation was done (user gesture or SJS-driven). Server gets tis in the request :reports the "destination" (where it's going to be used). Navigations also provide a target. get. 

Think about this as a Server side version of CORP. (CORP is from the server telling the client how to use the info.) With CORP, the damage is done, you're just protecting the user at the last mile. Sec-metadata helps servers mitigate the problem before is starts.

Google currently experimenting. 95% of services look to be able to deploy a CSRF-based policy on the server which is very promising! Would love to evaluate these results across more UAs and broader scope of the web.

Hadley: what's the performance impact?

Mike: 100 bytes to every request.

Dan: Web Devs aren't impacted?

Mike: expect most devs to ignore it, though it is there for inspection.

Mike: this is in Chrome behind a flag for experimentation. A few days to implement, a year for the Chrome Security rity rity Team to go test!

Mike: Would love critique, feedback from browser implementors. Landed a bunch of tests in W-P-T today, so should be fairly robust.

Mike: would love a better name too?

Dan: Could this be a breakout at TPAC? Any additional data you could have?

Mike: My objective is to make you all aware of this. I can corner some folks at various conferences.

Mike: "Sec-" prefix is purposeful--not settable by XHR/fetch.

Mike: One controversy (in initial version) sends 'origin' header on all of these requests. Pushback on creating another referrer header. Flipside--there is value in getting this. This was addressed by removing it in current version.

Alex: What's the benefit of Sec-Metadata on redirects?

Mike: we go through broader definition of re-directs. Header is re-generatored based on referring...

Data being sent is {kind: element}, site: { same/cross origin}, (if nav: target), (if nav: how). "kind" is based on "Destination" in Fetch spec table.

### Mike West Discussion: with-credentials

Yves: we came up with .. define a new error type when withCredential used and ACAO: *. Jonas Sicking was in favor of this. Something more specific then generic Network Error.

Mike: Is this part of the promise t?hen pipeline? 

Yves: yes, it would bubble out.

Mike: Seems fine. Data it leaks is fairly minor. Leakage probably has no real impact.

Dan: next steps Yves?

Yves: will make a PR. Have +1 from Jonas, Mkwest, TAG, Microsoft.

### Mike West Discussion: HTML Review (specifically issue 250; browser context and security )

Dan: what recommendations we would make about extensibility, deprecation. 

Mike: first pass: we we we we should figure out how to make new99-opener the default and target _blank . Sandbox es being eaten by Feature Policy which is good... (and giving a reference back to the opener)

Mike: Would also like to get rid of document.domain (relaxing the same-origin policy)

Mike: want to lock-down mime-types. Chrome considering restricting scriptable mime-types. Issue is so many scripts load HTML-as-script, and we can't lohack that down without massive web compat problems. (Hense CORB.)

David: can we lock that for module scripts and worklets?

Mike: Chrome already doing that for modules. Should do it for worklets if not already.

### Developer meetup planning

M/n  Starting at 6PM today. Planning details are not being minuted as - considered insignificant.

### Triage

Peter: We should triage and work on some of the non-HTML break-out sessions.

Travis: I can run the optimizer again to see how the split should look for break-outs.

Sangwhan: ISO-BMFF extra time should probably be removed, since we won't be able to arrange a call before the F2F is over.

(Working on logistics for break-outs)

### [Web Components Guidelines Doc](https://github.com/w3ctag/design-reviews/issues/227)

Kenneth: Domenic has made some comments on the document.

Alex: Ill have to ask him about this feedback. Currently looking at gold standard checklist, but it is a bit long.

Kenneth: It is. Does cover a lot of topics including accessibility though.

Alex: Slots is is a new capability for HTML - should touch on that topic

Travis: We could retrofit existing elements with slots

Alex: For no. 5 is this suggesting there should be a default behavior for elements whiwithout t a slot?  The behavior has changed - new behavior doesn't have a fallback. (Checking.) I don't think there is aduvice we should be giving here, probably best to remove it. 


Travis: There are attributes with complex syntax, which can't be created.

Alex: TThis is one of the problems we have . Properties and attributes are reflections of the underlying actual data, CE authors will need some form of internal storage to work around this

Travis: Should we note something about state, particularly suggesting properties over attributes?

Alex: dIdeally we'll have a private state storage mechanism, but that isn't the case now.

(eeDoing live updates on document.)

Alex: What is expected with the concept of default styling?

Kenneth: TI was proposing that it should have a minimum baseline functionality without having to resort on styling for the functionality - especially in a coupled manner

Travis: So thinking about styling in a layered way, and avoiding platform specific styling.

Sangwhan: Would this be practically do-able while making nice components?

Kenneth: I think it should. Stuff like animation shouldn't be coupled in.

Travis: Treeview would be an examplewhere the component would need sullch coupling though.

Kenneth: You could provide the default style unanimated and allow animating with a override

Sangwhan: But the logic behind the styling might not be practically possible if the default is designed around no animations (e.g. toggled with only display: block)

Travis: Maybe the recommendation should be about bediscouraging extreme cases of this

(Tweaking wording)

Travis: Is the concern that if you provide both property/attribute there would be confusion?

Alex: Yes

Travis: State would be out of sync if it is read out from the wrong place, since the state might not necessarily be up-to-date.

Alex: Attribute value should probably be the source of truth, according to the feedback here.

### [234 - automotive](https://github.com/w3ctag/design-reviews/issues/234)

Break-out: Dan, Hadley, Yves, Peter

[some discussion on the current CR and what our feedback should be]

### [237 - well known URIs](https://github.com/w3ctag/design-reviews/issues/234)

Break-out: Dan, Hadley, Yves, Peter

[hadley updated and closed issue]

### [240 - well known URIs](https://github.com/w3ctag/design-reviews/issues/240)

Break-out: Dan, Hadley, Yves, Peter

[discussion on use of DNS and other existing mechanisms for discovery]

**ACTION: Peter to write something up.**

### [241 - priority hints](https://github.com/w3ctag/design-reviews/issues/241)

Break-out: Dan, Hadley, Yves, Peter, Kenneth, David, Sangwhan, Travis

[Some concern regarding 4.7 - specifically around iframes and the implications for how this would be used for ads. What is to stop a 3rd party advertising provider from coercing the 1st party to marking all of their adversing content as high priority?]

Travis: could this be coupled with a feature policy that could turn it off for certain types of resources.


### [287 - Spatial Navigation](https://github.com/w3ctag/design-reviews/issues/287)

Sangwhan: generally the spec doesn't seem to have many issues. TV industry has been requesting it for a long time and it's not very well standardized. The "standard" approach has been the Opera approach (legacy). This has been an effort to standadrize it and give it an interface.  Issues : the security model in the context of iframes (hostile iframes). I suggested use of feature policy to mitigate.  Aside from that, no signifigant issues.

Dan: so do we need to do anything else?

Sangwhan: Aside from that I think we're happy. I found it OK. Another technical piece of feedback - given that we aaare recommending layered APIs, this is something that could sit in a layered API.

Dan: How does it related to hbbtv?

Sangwhan: they should be inyterterested. Median entertainment should also be interested.

Peter: no technical feedback yet. Naming of APIs... they are using "s'patnav" - they should use "spatialnavigation". And inconsistent use of capitalization.



### AOM - [134 - Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134)

(Guest: Alice Boxhall, Google)

Dan: Would it be possible to share the latest status?

Alice: The [explainer](https://github.com/WICG/aom/blob/gh-pages/explainer.md) is up to date... It allows idea is to allow programmatic access to the accessibility tree, and tallow R/W access to the AOM tree. The first problem was that the bootup cost was very expensive, considering the amount of users that depend on this. Problem two is that we need to standardize this across browsers, which was a huge task but deemed was necessary. The main bits that we had to touch on was WebComponents and Shadow DOM which has ID refs, and when it comes to crossing shadow boundaries it becomes complicated. We wanted to make a CE look and behave like a native elemen . WVisiting apage with a mobile client and voiceover enabled, there is no way to deal with slider-like components, as the intent availability from user interaction is not possible toaa announce. This is also a problem for cases lkeike canvas, where you need to declaratively define the AT programmatically to define what a raster buffer is actually showing. Still working on reflecting element relationships (setting and directly retrieving a element reference with an idref)ese, other implementors have stated that they would have issues with entering shadow root. There are also privacy implication - the existence of this itself is a privacy risk, some of this is being mitigtated by faking keyboard events in specific cases. The virtual accessibility tree case would still 

be affected by this. We won't be providing any slotting capability. The computed tree is still in early stages.

Alex: howhowHow does the idref issue solve anything?

Alice: That allows you direct access to the element, which lets you map two different things together. 

(Explanation about the characteristics idrefs)

Travis: TTThe cases you mention seem relevant, event handlers have unidirectional characteristics
hat
David: You mentioned obscuring the dddavailability of AT being a key factor, is this beneficial? II believe there are pretty reliable ways to find this out.

Alex: Yes, this is possible by testing timing differences, as creating and ilding uhousekeeping the accessibility tree is very expensive.

[Privacy Discussion](https://gist.github.com/alice/15ac1f8f147bc0648957ccd52e6de928)

Alice: Yes, this is all possible. There is a difference between fingerprinting and exposing this in the first place. From a user's perspective having a simple API that exposes this information in the first place is problematic.

David: There could be cases where this is beneficial.

Alice: This would be problematic in the virtualized UI (canvas and friends) AT, where ititnot exposing this would mnake the site nuunusable. This would be  case with CE as well, we are hoping in the virtual case we would probably only want to create only when the user needs it.

Alex: So modeled as a permission?

Alice: Yes, via permissions APi. Other options like media queries are being explored.

David: How do write operations against the AT reflect to the DOM?

Alice: It would need to be around a dirty ibit, with a refresh mechanism

Tcravis: Some points of feedback, internally discussed this. Semantic events preferrably being replaced with keyboard events.

Alice: Apple has been interested in semantic events

Travis: The second point is about the computed tree, what the browser' computed tree looks like and standardize that. When you start describing the relationships between the nodes certain aspects become unstable.

Alice: Coud ld you clarify  which tree? In Chrome there are at least three. 

Travis: iWQuite similar, I was assuming browser level accessibility tree. The relationships come from the UIA layer, and use that to navigate the tree. Would any of this be platform dependent? How about testing?

Alice: Hopefully not, and for tests against DOM and virtualized scenario it was done by testing whether or not the accessibility tree matches the expected value of the "superset" accessibility tree.

Travis: Feedback from our side is that the content authors would like to be a provider, instead of the browser being the provider. That would require exposing the raw AT APIs straight to to the application.

Alice: What kind of application is this?

Travis: Excel online. Different data model compared to conventional web applications.

Alice: This I believe is where the virtual tree comes in. The spreadsheet component of the app could be wired to a synthetic accessibiility tree.

Travis: Would be interested in wwparticipating  in this work.

Alice   : +1

Dan: ApWhat about other implementors?

Alice: Apple and Mozilla are involved and have been working on this.

Dan: So for our review, we should focus on the explainer?

Alice: Yes.

Dan: Anything in particular we should focus on there?

Alice: Been working on setting semantics on web components (via ARIA), and by setting these mappings on the shadow root it'es semantics would be exposed to the AT. Another source is definition options, which gives a list of IDL attributes. One extra topic is figuring out element reflection, whether we should follow what we did with shadow root. Still trying to figure out the spec. Not much to provide direct feedback on.

Travis: One approach we could try is to close this off, and review as the new features are developed.

Dan: Since Alice did mention the explainer we could review that.

Travis: I don't think we have objections on the direction.

Alice: Right now the explainer is all I have.

Dan: Anything we can do here?

Alice: Having a contact in other implementors would be great. There have been some communication trouble during development of the spec hopefully this will improve. Right now we need to sit down and find consensus.

Dan: We talked recently with the immersive web WG, and a11y popped up as a topic there too, has there been any discussion with this group?

Alice: AR/VR will most likely end up with interesting problems because the user interaction model is quite different, but we don't know exactly what problems we will encounter


### [queueMicrotask](https://github.com/w3ctag/design-reviews/issues/294)



### [DOM](https://github.com/w3ctag/design-reviews/issues/229)

### [WebUSB on Dedicated and Shared Workers](https://github.com/w3ctag/design-reviews/issues/277)

### [Async local storage](https://github.com/w3ctag/design-reviews/issues/278)

### [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282)

### [CSP feature 'unsafe-hashes'](https://github.com/w3ctag/design-reviews/issues/291)

### [Feature Policy JS introspection API](https://github.com/w3ctag/design-reviews/issues/292)

### [Stale-While-Revalidate handling in browser](https://github.com/w3ctag/design-reviews/issues/293)
