### TAG F2F
#### 7 Jan 2015 - NYC - Google - Earth

#### Present: Alex, Sergey, Yves, Domenic, Tim, Mark, Peter, Jeni, Dan
#### Regrets: Yehuda
#### Special Guests: Yan Zhu (morning), Sam Ruby (afternoon)

#### Chair: Dan
#### Scribe: Domenic

#### Topics:
- <a href="#HTTPS">HTTPS</a>
- <a href="#packaging">packaging</a>
- <a href="#capability">Capability URLs</a>
- <a href="#URL">URL-n-stuff</a>
- <a href="#captive">captive portals</a>
- <a href="#privacy">privacy interest group</a>

---

<a name="HTTPS"></a>
#### Topic: HTTPS 

(with special guest Yan Zhu)

mnot: We have [this draft](https://w3ctag.github.io/web-https/) I started thinking about this back when I saw the IAB statement on internet confidentiality, and thinking about it and the similarities between the IAB and the TAG, and was thinking that we should have a similar statement on the W3C side for the web. From an architectural standpoint especially, what can we state about the use of encryption and why that is or is not important. I wrote that down...

[discussion about how gists are not very good at auto-saving things you type and forget to save]

mnot: ... shopped it around to a few people, opened it up to the TAG. We've had a few issues raised on it; as I'm sure you all saw a fair amount of discussion on-list. Where we're at now I think is that we have probably some discussion to have today about it. A lot of the issues have been addressed to some degree; I'd love to hear what people think. Both in the large and in terms of going through the spec and making sure the language is appropriate; I am more than happy to take guidance on the specific language. There has been a kind of constant pressure to make this a very specific document, but I've been trying to resist that. Specific stuff needs to go in Recommendations; it needs to be a product of the consensus process. I also think the specific stuff needs to be taken care of by people closer to the matter. So in particular we have an Implementations section; my inclination is if anything to make it a little more generic than it is now.

dka: also see [Yan's blog post](https://zyan.scripts.mit.edu/blog/tls-everything/). One of the things I found interesting about the post is that it helps refute some of the points people bring up against the move to HTTPS. These are points that I hear a lot in various contexts, e.g. TLS are slow. I think it might be helpful to structure some discussion around your points. I think w.r.t. Mark's document, the abstract needs some work; I'm also curious how it relates to the document about [requirements for powerful features](https://w3c.github.io/webappsec/specs/powerfulfeatures/).

yan: note that the blog post was only a few things I've heard. You guys may have more.

timbl: a while ago the TAG said to the W3C, "can't you make everything available over HTTPS." However the webmaster said existing HTTP links would be impacted; it would be destructive to incoming links and internal links. He didn't want multiple caches for e.g. DTDs and so on. Given that we don't have any technology that allows browsers to understand that the "s" is irrelevant, we couldn't get him to move. And I sympathize completely since it's bad to break the links.

domenic: why can't you just 301 the http to new https links?

timbl: if you have a 301 then the people who link to http would be obligated to update their links.

domenic: ok...

yves: there's also an issue where even if HSTS is in place, browsers block http things as mixed content from a https context (See https://bugzilla.mozilla.org/show_bug.cgi?id=838395 )

yan: my understanding is that's a bug in browsers, and we're making progress on getting this fixed.

timbl: so browsers would have to go an check, like CORS preflight?

yan: no, they would use the HSTS preload list or they would use previous visits to sites. Browsers keep a list of sites that have opted in to HSTS preload.

timbl: so in the future we're asking for the web to contain all websites?

yan: I don't think anyone is suggesting that. With regard to preflight, the only way to do this is to try over https and see if it contains a HSTS header; if it is there then it's safe. I think this seems reasonable? But it's not in any spec yet.

timbl: it needs to be said clearly that any HSTS site is semantically the same with http versus https URLs. This is important for e.g. the semantic web ontologies. Almost none of the ontologies are HTTPS. Many don't even support CORS yet; it seems unlikely they'll get HTTPS and HSTS.

domenic: I still don't understand why e.g. w3.org can't move to HTTPS.

yves: that would mean old tools (e.g. SSL v3 only tools) would not be able to access the site.

domenic: first technical argument I've heard; thank you.

mnot: I feel like, both on the list and here, it's easy to get off topic. The focus of the draft finding is not "let's turn off HTTP today." It's about a gradual transition. I think even the most rabid HTTPS proponents can imagine issues with moving to HTTPS.

timbl: I think the document should list those

mnot: I'm not sure that's a good idea.

dka: I also think including some of the material, like in Yan's post, about common misconceptions etc., would be very useful. People have strong reactions, but I think it's intended more as moving.

timbl: I have a counterproposal. What about we migrate to http. We remove the "s". When people type "http" we use the TLS protocol, even when there's a "http:" in the URL. The "s" has left the web a horrible mixture of different things. Can you imagine if we encouraged people to move to IPv6 via "http6:". It's hiding the fact that the URL with-or-without the 6 gives the same thing. It's the same for "http:" vs. "https:", in most cases (except a few like the Forbes site Yan found.) How about that?

dka: in support of that, browsers don't show you the protocol anyway.

mnot: It's uncontroversial in the IETF that indicating security properties in the URL scheme was a bad idea. We talked about this extensively in the HTTP Working Group. Unfortunately with the web we have today, there's no way to make that transition; downgrade attacks would always be possible.

timbl: consider the user agent as trying to do something on behalf of the user. It could show the green URL bar even for "http:" if it is secure.

plinss: the fundamental difference is that if I try to connect to a "https" URL and it's not secure, I'll get nothing. However if I try to connect to a "http" URL and it's not secure, I'll still get the content.

timbl: you could get the content, but with a giant orange banner.

plinss: but there's no reliable indication to the browser that the site needs to be secure, to tell you whether the banner should be present or if it's just a normal HTTP site.

timbl: but that's irrelevant.

dka: haven't we learned that research has shown that nontechnical users don't understand the value of the lock icon anyway, and they believe a lock icon in the page is more important than a lock icon in the browser?

mnot: let's take this to a logical conclusion, with no https but a secure-over-http. Let's consider going to your bank. If you go to your bank and it's not secure, it will not serve you anything.

dka: my bank only does HTTPS for a login.

domenic: I think an insecure bank is not a relevant example.

mnot: back to my point, if we want to layer security onto the http URLs, the browser has to go to the site and decide whether it wants to use TLS. That discovery process is inherently insecure.

plinss: what if when you type "http://example.com" the browser first tried TLS over 443?

mnot: separate question, when you type "example.com", what about first trying "https://example.com". There are performance issues here, and also the case of HTTP and HTTPS being purposefully different.

[discussion about this kind of scheme]

mnot: the details of *how* to encourage HTTPS is a much longer discussion. For me I'd like this finding to set a longer-term goal and explore the space of what things need to be done, in our coordinating role as the TAG. Not a decision-making role.

jeni: I think this is really important it's really useful for the TAG to be making these kinds of statements. Reading it, I was left with a "aah! what am I supposed to do?" feeling. I think answering that would be useful. There are some specific things around how to handle mixed content, from a data-serving point of view, saying that if you're serving data on the web you should be thinking right now of how you're going to move to HTTPS. I also think that flagging up the transition stories in more detail would be incredibly helpful and would help explain that this will be a longer journey and help give practical steps.

mnot: that brings up an interesting point which is who the audience of this document are. You said "you" don't know what to do next. You in which sense?

jeni: me as a publisher

dka: "webmaster"

mnot: personally I think the audience for this document should not primarily be web developers and content producers, because it is a *huge* issue for that audience that is bigger than can be captured by a TAG finding. I'm looking for something much closer in scoping and audience to the IAB statement, which is "Hi, standards body: we're your architectural group, and this is the direction we need to go in."

jeni: that's fine, but I think it needs to be more clearly stated.

timbl: that said, even if things will get worked out in other documents, it's important to have an "issue list" included.

jeni: I agree. If this is the direction we need to move in, then it's still important to list the specific things that are problems and that need to be addressed, is helpful.

domenic: I'm not sure. This is supposed to be a statement that stands the test of time, on the general idea of encryption on the web. Specific technical issues are temporally local.

jeni: I think that's fine but in that case there needs to be two documents.

dka: I think it's important to enumerate those things because people will try to use them to rubbish this document. It's especially important when we can refute them, e.g. performance. It helps clear the way for the vision.

mnot: I'm happy to add if this makes you more comfortable, but I am fascinated that we feel the need to justify ourselves, when the IAB document did not include justification and was accepted universally.

domenic: I really don't think those people are our audience.

timbl: I think it's not doing our job if we don't address those issues. Maybe the IAB and TAG are on different levels.

mnot: I have a counter-counter-counter proposal. I think this document should be very brief. Two or three paragraphs; high level; we can open a number of issues and link to them.

alex: I am not sure that would be productive, because when we are engaging with working groups, they will have a series of questions that we'll have to answer, and it would be bad to answer them ad-hoc. It seems to me that part of the utility of this document is a coherent and concise explanation of why this is a good thing to do.

mnot: I just don't want it to be an issues list. Issues should be in the issues list.

domenic: I love that, just link to the issues list.

dka: no, the document needs to be self-contained.

mnot: I don't disagree, but I'm a little uncomfortable with how verbose the document is now. What is your proposal in terms of the current document?

yan: one of the things I've noticed from anti-HTTPS people is they complain about costs; we should tell them about the benefits and that will answer lots.

timbl: one thing I've asked for is a comparison of round trip times. Nobody has given that to me.

mnot: there's a lot of permutations; 0RT vs. 1RT; (a few other technologies I didn't catch); there's a matrix---it's pretty complex.

domenic: best case scenario is zero extra round trips with properly configured software.

https://istlsfastyet.com

https://www.igvita.com/2013/12/16/optimizing-nginx-tls-time-to-first-byte/

timbl: that's pretty amazing. what about client certs?

mnot: client certs are kind of a corner case but also used enough that we can't ignore. But they're not recommend and I'm not sure where they come in to things. In general there is lots of old software but there's a lot of work going in to making TLS have less and less overhead from a user-perceived latency standpoint. Certainly on a standards timescale we can rely on that.

dka: back to the document. We could say something like "some people say there's performance issues but the consensus in the deployment community is that these are addressed or in the process of being addressed."

mnot: so, the document already talks about performance. What is your concrete feedback in terms of deltas? If I have to rewrite it from scratch, I will, but I'm not sure what exactly the TAG wants at this point.

dka: I feel like there should be an issues section, both containing issues and explaining mitigations, to clear the air of objections that might potentially be in peoples' mines.

mnot: [reads from the document]: "Historically, the perceived performance of HTTPS has been worse than that of cleartext HTTP, because of the protocol ovpackaging
erhead. However, rCapability URLs
ecent developmentsCapability URLs 
packaging 
 such as HTTP/2, OCSP Stapling and TLS session tickets have reduced this overhead to the point where the deficit is minor -- often, inperceptible (see Is TLS Fast Yet? for details). We expect that future developments (such as TLS/1.3) will further reduce the performance penalty of encryption."

domenic: comes down to audience and vision for this document

mnot: so the feedback is largely about document organization, OK.

dka: also should we include something about "http:"?

mnot: that seems too speculative

domenic: seems like the domain of the IETF

timbl: I worry that when the IETF discusses protocol-level stuff they don't think about a web of links.

mnot: as domenic was saying earlier, people in the HTTP world would say the answer is 301, and don't understand why that's a problem.

timbl: there is impact on the semantic web community where they compare strings instead of comparing resolved URLs.

[discussion of semantic web comparing URLs as strings and how this works with a web full of redirects]

dka: is there something we could say in the document about equivalence of "http:" and "https:" that would be forward-looking

plinss: I think we should publish mark's document like it is but also publish a document about best practices for deploying https where we can say things like "your http and your https should be equivalent."

mnot: I would hope we would focus on the content implications of the conversion.
res[e
plinss: I agree, but it should be a separate document.

[discussion about default apache configuration]

dka: relates to [what w3c currently tells "webmasters" about configuring security](http://www.w3.org/Security/faq/ ). You don't even want to look at this page; it will burn your eyes. We should make a new version of this and deprecate the old one.

mnot: so in general the idea is a few tweaks are used.

dka: I think the wording on the caching section is a little dismissive.

mnot: I am uncomfortable using this document to predict future approaches to caching.

timbl: this document is about the current situation.

domenic: I re-read the paragraph and don't think it's dismissive. But if there's a concrete change you'd like...

[discussion of the paragraph in specific]

[discussion of gogo mitm'ing websites]

dka: yan, anything from you?

yan: in general I thought mark's draft was quite good, and if anything it could be more promotional of https.

plinss: any thoughts about peter's second best practices document?

yan: seems like a good idea, but keep in mind that things will be changing rapidly.

plinss: I was thinking more about high level things like equivalence of http and https content; use of HSTS; etc. also looking toward a future of secure "http:"

alex: it seems to me that sunsetting HTTP is isomorphic. I agree that once common user agents mark HTTP as insecure, and put friction in the way of visiting HTTP websites, it will change peoples' view of the old, unmaintained web that is not upgraded to HTTPS. For most purposes it will be unsupported (although you can go digging for it).

plinss: I'm fine with that, I just don't see that needing to be predicated on the "s" in the URL.

dka: agree.

[discussion of secure "http"]

plinss: the difficulty is that you want the site to fail when insecure.

[discussion of three documents: Mark's finding; best practices; and secure "http:". The second two are potential new work.]


<a name="packaging"></a>
#### Topic: packaging 

http://w3ctag.github.io/packaging-on-the-web/

dka: given that Jeni is leaving, we should talk about packaging

jeni: yves, do you have an update? sense it went to webapps?

yves: I think a CfC was sent, but I don't remember what happened next...

jeni: that's where it is, as far as I know.

yves: it was not published after the CfC deadline. So I will check with the chairs to work on that.

[ACTION: Yves to check with chairs on webapps on packaging...]

domenic: more on the topic of progress instead of Process, what's the implementation status?

jeni: none that I know of; there was talk of building on top of service workers at the last F2F.

alex: now that service workers are shipping, builing it seems like a weekend project. It will only be demo-ware since service workers do not work on first load. where are we with any issues on it?

jeni: the issues I'm thinking of are the ones Dave raised at the last F2F he attended, back in April. He raised that Jonas was concerned about something or other, but couldn't really articulate what that was.

alex: doesn't seem like actionable feedback. OK, so now that we have a packaging format, with issues that we can't identify (which seems like a good place to be), I'm curious about how we could go about providing signing for that packaging format. You could provide a signature out of band, e.g. in the meta tag. Or it could be in-band, presumably at the end of the bundle?

[discussion of signature position]

mnot: I'd really hope that this would not be reinventing HTTP.

alex: let's say you'd like to create an application system where you're only running known code, previously identified as trustable in some context. Well if all of the code comes out of a package, and you can sign that package, you win.

mnot: in HTTP you would do this with the headers in the package for each resource.


alex: who uses HTTP for signing?

mnot: oauth, web payments, jose

yves: isn't there one about saying there's an alternative representation in some other place?

mnot: ah yes, metalink. a really cool spec, used a lot by download agents. rfc 6249

jeni: so it might be nice for the packaging spec to explicitly include an example of how to do this kind of signing.

mnot: I'm going to send this to the webperf working group since it makes performance claims, and also to the apps area working group in the IETF.

jeni: FYI the reason I am leaving the TAG is I don't have time to commit to moving this forward and taking such comments.

dka: so I think this needs an owner. yves? sounds good. yves is going to be the owner.

alex: from my side I will try to rustle up implementation interest. I think we're at a point where we just need to do it.

jeni: let's go through the issues. One is saying that zip can be streaming

alex: we discussed this at some length. zip might work for streaming in the most technical sense, if you trusted the per-item entry names. but the argument that sealed the deal was the need for headers.

[we are looking at issues in packaging spec and closing them / discussing]

https://github.com/w3ctag/packaging-on-the-web/issues

https://github.com/w3ctag/packaging-on-the-web/issues/13

Mark: whilst liaison is good and we might consider using that if it's ready, this document is about [doing something that works with existing formats...]

 https://github.com/w3ctag/packaging-on-the-web/issues/12

<a name="capability"></a>
#### Topic: Capability URLs 

DKA: As far as I'm concerned this is a published finding.

Jeni: Some issues have come up in github - suggested changes.

https://github.com/w3ctag/capability-urls/pull/5

[discussion on this topic]

[Resolved to make appropriate chanegs to doc, Jeni to continue to be attached to this unless workload gets too high. Yves will finalize getting it published formally as an approved finding.]
URL-n-stuff
URL-n-stuff 
URL-n-stuff  

---

#### Scribe: Dan
#### Chair: Peter
#### Guest: Sam Ruby

<a name="URL"></a>
#### Topic: URL-n-stuff

Peter: Let's start.

Sam: https://url.spec.whatwg.org/interop/test-results/

Sam: The URL spec [whatwg] had technical issues - test failures. [See https://url.spec.whatwg.org/interop/test-results/]. Confirming URLs I've evolved the whatwg standard to be confirming URLs are a subset of URI references. Even so, some differences - departures from the spec in the existing implementations. In some sense the problem reduce the impetus for people to change. I'd like to come out of this with at least a subset that [is guaranteed to] work. These were the test cases that were put forward for the transition request.  Trying to motivate people to discuss this.  URLs are an important architectureal [component] of the web.

Mark: the space of URLs is huge. A lot of these test cases are valid in the RFC-3986 sense but not in the [general use?]. 

[discussion on what "conforming URLs" means]

Sam: I've evolve Anne's spec to have every contraint that I can find in theexisting epsecs.

Mark: looking at test 11 - IE is highlighted yellow because it's port 80 / that's not functionally different

Sam: it should be consistent. People at Microsoft are interested in this / I can get them engaged. They are focused on a new release right now.

Mark: We could filter out the default port issue, paging around it looks like there's still a lot left.

[discussion on the Python library...particularly how old and grotty it is]

Sam: https://github.com/webspecs/url#the-url-standard is the verison I am working on. Changes will be mergerd back into the whatwg version when it's ready. My goal is to broaden the number of people participaring. This will go back to whatwg. Anything pushed back there I can push back to the TAG repo.

Dka: do we need the TAG version any more?

Sam: yes possibly - some people want stable snapshots. when it gets to that point you know it's been widely reviewed, etc...  on the URL standard I can get this to the point where it's good stuff with more [future-loooking] features split off. Whatwg isn't currently set up to 

Sam: plan was end of q1 to have a stable references to the URL spec. No options off the table. one possible answer is to have a living standard and stable snapshots, possibly hosting snaphots at w3c. would argue against changing logo / copyright / etc... but would argue for a stable snapshot.

Domenic: i think it's problematic to how it's currently done. The fork in the tag repo is not a result of collaboration.

Sam: I think there is some collaboration.

Sam: Next level of the plan - on the web platform docs URL standard, under work mode: 

Mark: other question - a lot of these [tests] seem like - how confident are you - you're deriving behavior of browsers using a javascript library. 

Sam: using A tags.

Mark: Ok - that answers the questions

Sam: So far I have not rejected any input.

Sam: We also need more tests. 

Domenic: I should contribute the node.js tests.

Tim: looking through the API - is it too high level to crtitcise it for not having a serializer relative to the base.

Sam: At the moment it's basd on what's implemented.

Sam: given a result and a base, what would the reference be?

Domenic: I think it's useful.

Yves: do you have testing data on what proxies are doing.

Sam: not yet but I could do that. More tests is good. More filters is good.  The tool has a lack of input.

Domenic: a lack of implementation - browsers have not updated their parsers.

[discussion on file URLs and whether they should be specified or left to implementation]

Domenic: when you put a href with a file URL in it what happens - it's not about what you type.

Sam: some are sitting on the sidelings because it's not endorsed by people they care about.

DKA: we should continue to add positive reinforcement to this.

Sam: on work mode, https://github.com/webspecs/url/blob/develop/docs/workmode.md#preface [enumerates points there]. 

Sam: https://specs.webplatform.org/url/webspecs/develop/

Tim: is there a GH pages page?

[discussion on unicorns]

Sam: I 've added railroad diagrams and it's split up more functionally. 

Sam: I can put it on github pages.

Domenic: we need as many URLs for the URL spec as possible.

One implementation of   refTo and join:    https://github.com/linkeddata/rdflib.js/blob/master/uri.coffee
Another (old python) one https://github.com/linkeddata/swap/blob/master/uripath.py

PLH: you don't have PHP [in your implementation list]

Sam: [I could.]

Domenic: we all want everybody to parse URLs the same way - to get there is a long and hard process that Sam has volunteered to work on - the clients that we should look to are the browsers - then we have to look at the edge cases where others discsagree. We need to create a coalition of people who start agreeing [to engage e.g. PHP URL parsing].

Sam: I agree with that goal - browsers will be the tail that wags the dog. Some people say "you start with RFC-3986". 

Mark: I think getting more data about the real delta would be good.

[discussion on some other implementations]

[discussion of layers that I'm not understanding]

Sam: whatever you throw at a URL parser, the output is a proper subset, a document that describes that subset might be useful. An interesting criteria of outputs is that they should round-trip.

Tim: a discussion we had a while back in the TAG with Larry & Roy - related to cannocalization. TAG looked at it and noted that there are different levels of cannonicalization - TAG pointed out that you can think of this as a ladder - when you know that somethings a domain name you can c-z it to lower case. you can remove ./ - further down the line you can use knowledge of http spec to do more c-zing. does it c-z DNS names to lower case?

Sam: yes.

Tim: Does it remove the ./

Sam: yes.

[does it remove slash-dot though?]

Sam: ultimately what the browsers do - people will converge on this.  Example of a no - %xx - it will not lower-case or upper-case those things. At the moment the browsers have said "juts leave them alone." There are implications - e.g. cache misses.

Domenic: you could imagine a def of c-zing where this would be the same.

Tim: The TAG has said "there is no one c-zing". Different systems will apply different levels of c-zing by applying knowlegde about the relevant specs.

Sam: Part of that shows up in 3987.

Sam: everybody implements something like URL.parse - if we could all agree...

https://url.spec.whatwg.org/reference-implementation/liveview2.html#http%3A%2F%2Fexample.org%2Ffoo%2Fbar%20http%3A%2F%2Ff%3A00000000000000000000080%2Fc

[discussion of test page details]

[discussion of perhaps using a CSP directive to force translation of "http://" urls to "https://"]

timbl: there are cases where it's reasonable to give users some control over relativeization in some cases. A standard API might have preferences for this sort of thing.
captive portals
privacy interest group: http://www.w3.org/Privacy/
captive portals 
privacy interest group: http://www.w3.org/Privacy/ 

sam: there are lots of cases where this doesn't make sense; we can do that if it makes sense to end-uesrs -- IDNA is a place where options haven't helped

sam: my interest is in getting people engaged in this process

[break]

[possibly back from break...]

Sam: Work-moe stuff. Question do we still need the TAG version. I still think there is a value to stable snapshots being published in a recognized space.

Mark: In IETF you just publish an update.

Sam: I can i take the content of the spec and make changes [3986] or do I need to start from scratch?  If it's a delta on the existing spec then I'll get more people engaged.

Mark: the general feeling is that if it's a legitimate input to the standards process then you have cover.

Mark: ping Roy and say you're going it to do it. 

[discussion of doing the new IETF draft as a delta vs. a new doc]

dka: do we need a new IETF draft at all?

[general agreement that in an ideal world we would have only one spec]

[discussion on Gopher - for some reason]

[discussion on veritcal bars in context of file URLs]

Sam: Suggesting we could use the same model for the streams / fetch specs as we are attempting to use for the URL spec - w3c-published snapshots.

Dom: Yep.

Plh: Fine.

Sam: can we get more people involved?

DKA: I can make suggested editorial changes - e.g. approaching the document from a naiive reader pov and adding bits fo editorial to clarify, etc...

Sam: If it's stuff like status text you can just do it as pull requetss in the web platform version of the document.

[ending discussion on URL]

<a name="captive"></a>
#### Topic: captive portals

mnot: there's a proposal that's getting traction about a DHCP flag to note captive portals

[what's the background?]

mnot: the proposal is a DHCP option that includes a captive-portal URI as part of the response; the connection wouldn't be "active" until you register with the URI

timbl: network access is blocked until you visit?

mnot: there's perhaps some difference what the authors intend vs what will get deployed

mnot: there are cases where portals try to work around the OS's protections and they are teh most interesting

timbl: why would they do that?

mnot: not sure. Need to talk to them more.

timbl: we've heard about the cat/mouse game Apple has had to play with these systems.

mnot: need to get people in a room

dka: why has it taken so long?

mnot: lots of people who run portals don't play well with others. It makes it hard to coordinate with them. Big companies are starting to do more of this, though, e.g. Verizon.

timbl: how else can one persuade them?

timbl: there seem to be 2 kinds: folks who are trying to do the right thing and folks who aren't. You can imagine something (the OS) leaves open a "thanks to our sponsors". If you're Google/a University/etc., you can imagine just want to require them to accept terms/conditions. Terms/conditions could be in a JSON format or something that allows you to come up with a protocol about neogiating access.

[discussion of AT&T, payment, etc.]

mnot: there's a discussion to be had about endgames; what do we want to encourage or discourage? lots of people are just handing out passwords now (more hotels). We don't want to encourage captive portals

plinss: a lot of US hotels are giving out passwords, but they're passwords to the cpative portal, not the network.

timbl: BA might be an interesting case...they want a way to introduce you to the airline/hotel's home page...

dka: my hotel gives out wifi if you're a member of the loyalty program.

mnot: there's a new kit that's actively attacking captive portals and MITMs users by cloning the captive portal.

[discussion of DHCP security]

[discussion of legal environments where you aren't allowed to give access to strangers]

plinss: what would it be like to create a "trustable captive portal"?

mnot: that's why you want to put it in a separate UX from normal browsing.

plinss: would be nice if it _were_ part of the wifi handshake

plinss: we've talked about getting people together at TPAC, anything else we can do shorter term?

[it's a long slog]

<a name="privacy"></a>
#### Topic: privacy interest group

http://www.w3.org/Privacy/ 

dka: there is a privacy interest group in the W3C...a doc that describes privacy considerations for API design.

dka: they were looking for a privacy review for all new specs.

dka: perhaps we need a call with them? their chairs could introduce their work.

slightlyoff: it'd be great to get on the same page with them about what aspects of privacy they're looking at to make sure we understand each other

FINI

