## TAG F2F - London
##### 01 February 2018

Present: Dan, Peter, David, Andrew, Alex, Lukasz, Travis, Hadley, Yves (remote), Sangwhan (remote)

Regrets: Tim

---

Scribes:
 * Wed AM: Travis
 * Wed PM: Andrew
 * Thu AM: David
 * Thu PM: Alex
 * Fri AM: Hadley
 * Fri PM: ?

### [HTML General](https://github.com/w3ctag/design-reviews/issues/174)

Dan: We had this HTML issue that we discussed briefly yesterday, wanted to discuss when Sangwhan back.  We were thinking about decomposing this issue, to try to make it more digestible.

Travis: On my team at Microsoft, we're trying to find a way to better track the changes that are happening in the HTML spec.  Too large a responsibility to give to just one person.  So we haven't yet done this, but I aspire to sit down and think how to logically separate the big pieces of the spec into digestible chunks.  I suggested I could bring this information back to the TAG so that we could do something similar for TAG reviews.

Sangwhan: Realistically tackling in a face-to-face is impossible.

Dan: Can we decompose the topic sufficiently to make progress.  We talked about doing this in Japan last year, haven't made much progress.  We need to do something to break that down.

David: Maybe devote more to new things than things the web is stuck with.

Alex: Yes.  But should also highlight areas where better layering will open opportunties.  For example, when it comes to forms... Shadow DOM.  Unclear what the right form to highlight that.

Travis: Goal of creating new work to deconstruct those things.

Alex: Pointing out important areas for new work to start in.

Travis: Sounds good.

Alex: &lt;input> elements are a gigantic pile of fail.

Travis: Another area of discussion yesterday was topic of conformance criteria.  How much are we interested in to paying attention to bits of spec that are just author conformance criteria -- things that aren't enforced by implementations.

Sangwhan: Honestly not sure if conformance is the right word for this.  Not sure how to tackle this problem.  Some consider validator.nu authoritative.

Travis: Annevk replied to our issue with some of his thoughts.  Helps with forward-compatibility and allows expanding the feature set over time.  With a markup language the infrastructure is set up to parse any named element into an element.  Doesn't do anything particularly useful, but leaves open the opportunity to define new elements in the future.

David: Not sure how much of that is the author conformance requirements vs. implementation conformance requirements that define error handling.

Travis: The conformance requirements about one &lt;main> came up yesterday.

Travis: Question is how should we spend our time for this issue?  Happy to take my offer to propose a way to split it?

[agreement]

Travis: OK, I'll take that.  Come back at end of month?  27th.

### July meeting location

Dan: We have more flexibility for July meeting location.

Dan: Travis, want to do the Seattle meeting in July rather than October?

[discussion about a European meeting more adjacent to TPAC]

Hadley: Maybe valuable to meet right after TPAC, can discuss things that are fresh in our minds?

[discussion about London vs. Nice vs. Paris]

David: could host at Mozilla Paris

Zeroing in on July Seattle (Microsoft), October 30 - November 1, Paris (Mozilla)

Brief discussion led to choosing Tuesday-Thursday dates for Seattle as well.

### Fake news<a id="fake-news">


Hadley: I put together [a document](https://docs.google.com/document/d/113N3vJ8x3fmyL9ZbNUwdGwEP0QRwBWkgiFHWv7tnUsE/edit) as the beginning of an explainer.  If the problem is that services trying to do good (crawlers, UAs, news feeds) -- if they want to try to prioritize good or bad news, they don't have much machine-readable data to make that distiction.  Main thing they have is popularity, which optimizes for outrage.  There's potential to build up information about the domain.  Isn't necessarily a 1:1 mapping of content to domain.  What I want to do, and what I want your feedback on, is primarily having more machine-readable information.  In a perfect world fake news would label itself as fake, but that's not realistic.  So we have to give good/effective news the ability to distinguish itself.  I think some kind of markup to be agreed with news and publishing industries to demonstrate things like provenance of facts, source of quotes, etc.[[Citation Needed]]

Alex: so transparent news.  Not so much not fake as attributable.

Hadley: I think also something about reputation of the journalist themselves / the author.  Since at some point you're looking at things like leaks from the white house, which aren't attributable.

Alex: But in that cause you want the identity of the author to be attributable.  So looking for content attestation.

Hadley: So I think part of the solution is the news itself being able to say things we can trace about that news.  Part is that people commenting on or reviewing other articles can be understood in machine-readable way.

Lukasz: How will you provide markup for justifying the facts?  If article is based on investigation or sources you can't attribute?  This would only work for articles based on other articles.  Only references to other articles.  How does this differ from links?

Hadley: A lot would be links, or attributes on links saying why those links are there.  But as I was saying a minute ago, a lot of news is based on things that happen offline, and we need to study reputation of journalist or organization.

Lukasz: Also need to distinguish between fake news meant to gather clicks versus a deliberate misinformation campaign.

Hadley: We need to be clear what use cases this will address.  Another thing I worked out having this conversation.  Some people use fake news to mean memes, images, videos.

Lukasz: I agree fake news is bad, harmful to web.  Does fixing this at web standardization level feasible?

Hadley: That's exactly the question to ask.  I'm hoping this is a way we can help, but it won't solve all the problems of bad information on the Web; Web founded on free speech.

Lukasz: Relies on the way users consume news.  User interface and web design

Hadley: 
[ lost a bit due to cryptpad glitch ]

Dan: One example of how the underlying technology of the Web can support... As we talked about in our [https://www.w3.org/2001/tag/doc/distributed-content/](Distributed and syndicated content finding), we worry about rehosting approaches like AMP because they take away from the user the option of knowing the domain that has published a news article. For example, if I read an article that's on nytimes.com then I know it's from the New York Times, especially given https: and domain.  This an example of how architecture helps determine provenance.  Things that undermine that potentially open door to more fake news.

Travis: Architecture guarantees the source being an origin.  Intuiting the goodness/badness of the origin isn't part of the Web architecture.

Hadley: I don't want use to make those value judgments, but I want to help others be able to make those judgments.

Lukasz: If you introduce markup for linking to external sources.  People can use markup to link to other false information.

Hadley: I want to allow other sites to make clearer assertions about their evaluation of a particular site.

Travis: Like Alex said earlier, we could try making a more direct relationship between articl's author and identity behind the author.  Can then layer assertions about the author.  Like origin is an important piece for content distribution, identity needs to be associated with the article.

Dan/Lukasz: keybase

Hadley: I think that's one way to do it.  Something in the idea you're talking about that's wikipedia-ish about connecting to previous career/publications of the journalist.

Travis: Articles can be jointly published, by a community, etc.

Peter: We've talked about signed content or packages, does it make sense to have signable elements, where you can sign a chunk of a document.

Alex: It would be possible... long live HTML imports.

Lukasz: Could use Subresource integrity.

Peter: I'm talking about for a &lt;div>.

Hadley: Alex, where were you going?

Alex: If you're replacing the content of an element.  If you have a &lt;my-article> element that presented content.  You could potentially have the contents of that come from a signed subresource.  It's not part of the toplevel document, which creates problems for indexability & understandability.  It's not clear what that gets you.  To Lukasz's point, you can use SRI and script to inject the content; we don't have declarative transclusion.

Lukasz: Mentioned more like extending SRI to element contents, but just as an example (attestation). It would address the problem where somebody links to something and then the thing they're changing to becomes something outrageous afterwards. But might not be the thing we want?

Hadley: I haven't done the definitive research on this, but I'd love to see evidence that verifying identity of article author is a problem... it may not be a problem.  It may just be that asserting that a certain person is the author of the article is good enough.


Andrew: I think authorship is in an important factor.  I think ... sign the content to verify it hasn't changed since written.  But doesn't directly address accuracy.  The issue of acuracy is one of sourcing and provenance.  The author might have great reputation amongst their followers but they might still be spouting rubbish.  You can great reputation if you find enough people to agree with you, but you don't have to be right.  So there are ways that this can be done to highlight sourcing information in articles, e.g., crawlers that have enough intelligence.  If you have enough of those references you can establish that something that's blown up all up over the web is all based on a single thing that's wrong.  I think that's something worth addressing more than authorship.  At the FT I tried to set up something where we'd list sources in sidebar, and rate them, e.g., for transparency.  There's a list of euphemisms (e.g., "a person familiar with the matter" is vaguest), and you pick the most specific one you're allowed to use.  Be more transparent about what we mean by these expressions and assign ratings to them.  Be transparent that sources for 2 stories were the same.

Dan: You could correlate the information and use to deanonymize the source.

Andrew: "someone familiar with the matter" shows up in thousands of stories, but you have no idea which are the same.  It's not a codename, just a description.  I was trying to assign it a codename.

Lukasz: [Florida Man](https://en.wikipedia.org/wiki/Florida_Man)

Lukasz: some examples of fake authors might be [here](https://www.nytimes.com/2017/09/07/us/politics/russia-facebook-twitter-election.html).

Lukasz: You wouldn't solve this with web architecture changes.

Hadley: None of these approaches are perfect, but I want to expose more information across the board so UAs and crawlers can make better decisions.

Dan: It strikes me that:  are there things like our [https://www.w3.org/2001/tag/doc/web-https](securing the web) finding or the distributed content finding that could come out of this and help provide positive reenforcement to activities that are already happening?  What other areas could we support in service of these goals?

Hadley: I think this will be ongoing work for a couple of years.  What I was hoping for at this meeting was your preliminary thoughts and reactions, and if there are any specific concrete areas of work.  Yves mentioned community group working on credibility.

Lukasz: Transparency something that is definitely worth work on

Hadley: In due course might want to issue TAG statement in a few meetings.  Maybe a finding.

Dan: Maybe rather than having a finding about fake news, I'd rather do findings of the kind like https-everywhere thate are supporting a specific initiative.  Where we could support an initiative and note benefit of working against fake news.  https-everywhere mitigated against surveillance, script injection by commercial actors.

Lukasz: but no tech movement here

Hadley: We're in a position to help create the movement, but help lay out set of initiatives that can be delivered as set projects or features on the web platform.  On the topic of fake news these are areas of work that are helping to solve the problem.  Let's set the big picture and cheer on everbody helping to solve that.

Dan: would workshop be helpful?

Hadley: I feel like it's too early. Can we have that conversation at our next face-to-fcae?

Dan: Would it be good to get journalism organizations together?

Dan: Coming back to HTTPS finding, one of the things that came before that was the [joint W3C/IETF strint workshop](https://www.w3.org/2014/strint/) that brought people together and that ended up being a big deal... in terms of what came out of that afterwards.

Hadley: Not yet at the point where I could frame the call for proposals.

Lukasz: Fake news is not a matter of journalism.  EC recently created expert group on fake news, with representatives from media companies, but not experts in disinformation campaigns.  What would be the outcome?

Dan: Outcome of any workshop like this would be a series of technical initiatives that might help to mitigate issues.  Point of involving journalism organizations (not necessarily journalists), to address their real issues.  We think we know about news but we're not journalists.

Lukasz: I want to make sure we understand the differences with TLS.  If you have fake news or disinformation campaign it's more esoteric.  You could also classify TV advertisements as fake news.  But this is legitimate fake news.

Hadley: If we do this workshop we need to frame the CfP very specifically so we have the conversations that we want to have. You're right that there are a lot of uses of the term "fake news" that wouldn't be helped by these changes. 

Lukasz: There are many conversations happening.  What's the value of another one?

Hadley: figure out what we can do in terms of architecture of the web

Dan: also value of bringing people from different perspectives together for a few days.

Hadley: e.g., if we created markup we'd need news organizations to produce it.  We'd need everyone who has an interest (or is currently saying they're being hurt by fake news initiatives) to help us define use cases. We'd need UAs and crawlers/indexers to tell us what they would consume. 

Lukasz: Would it be useful to have input from researchers or regulators?

Hadley: Could be, depends on how we frame the question.

Lukasz: Motion in European Commission in this scope.  Don't know about US.

Hadley: We do try to stay away from regulations of any one jurisdiction.

Lukasz: Different countries in Europe are taking their own initiatives here.  Would need to produce something that's implemented and actually used.

Peter: Love the approach about creating some kind of market / ???.  But we'd need to seriously red-team it, to avoid creating a tool that the troll farms can use to claim legitimacy.

Hadley: Absolutely 

Lukasz: any open solution could end up abused. TLS can also be used by phishing sites. The thing is not to facilitate further abuse

### [Image Decode](https://github.com/w3ctag/design-reviews/issues/182)

Sangwhan: This just needs to be reviewed again.  Having somebody else look would help.  I think our main feedback was that we didn't like the name `decode` since it was a hint rather than actually decoding it.  Maybe I could take a look and we can revisit in the afternoon or tomorrow?

Dan: Punt to tomorrow?

Andrew: My thoughts same as before.  Issue of naming not that it clashes in the same, but that it sets a precedent for an  understanding of what "decode" means, and it's bad for two methods on different things to have the same name but do different things...

Alex: on the same kind of entity, e.g., decoding audio samples is different.

Andrew: We're talking about two things, one being implemented now, and one that might be implemented in the future.

Dan: Could see if there's TAG consensus on this point.

Sangwhan: Fundamentally an HTML &lt;img> element isn't exactly an image;  I get what they're talking about.  Web developers are used to APIs doing not-so-straightforward things.  Since HTMLImageElement doesn't represent exactly an image, I guess the second part is:  why do we not have a proper decode api, but that's probably not for this issue?

Andrew: That's the point I'm making.  If we did have a proper decode API, what would it be called?

Sangwhan: It wouldn't be on HTMLImageElement.

Andrew: But it would still be confusing, even on something different.

Alex: Argument here is that "decode" is a verb, and you're asking the thing on the left of it to be decoded.  The API here is advisory, a hint, or a "when decoded".  The current name is not *on*, and I agree with that.

Sangwhan: Let me try to reword and get back on this review issue based on feedback we have.  And I need to look at changes in the proposal.

### EU GDPR/ePrivacy Regulation and browsers

Lukasz: I'm concern about GDPR requires consent, and a specific reason for using data.  And some sensitive APIs do not have support for that.  So sites have to consent on their own.  I'm wonder if it wouldn't be good idea to add "purpose" specification to applicaitons, so if someone wants to access geolocations, there would be an option with a message that could be interpreted by UA and maybe shown to the user.  It's actually working similarly in iOS. So this is about consent (?).  GDPR is a large thing; difficult to tackle all things in a session.  

Lukasz: For ePrivacy, work is ongoing.  Euorpean Parliament would require web browsers to implement DNT in some specific form.  Was controversial back then.  It will be binding signal from the user.  Now ePrivacy is not defined yet in the European legislation.  The actual end requirements aren't known yet.  I'm keeping track of that.  I don't think those requirements will arrive this year.

Dan: Thought with GDPR in May.

Hadley: Still being informed, whereas GDPR done.

Lukasz: The most ??? version is passed by European Parliament.  Has strong requirement in DNT, also sensors.

Hadley: How different from versions in European Commission and European Council.

Lukasz: much more strict

Hadley: so when all versions come together?

Lukasz: There will be a fight.

Lukasz: GDPR is in May.  It's already working, but not being enforced.  Data protection authorities are busy with specific guidelines.  Don't expect web-related specific guidelines soon.  One thing that came to my mind was the consent. As for the DPIA, it's the responsibility of vendors.  Someone opened issue in W3C Web Payments WG, that W3C should prepare data protection impact assessment of the API.  I don't think W3C needs doing that.  I don't think W3C is responsible for creating data protection impact assessments.

Lukasz: There's a requirement to creating a data protection impact assessment in relation to processing.  The idea was that if W3C made one, vendors would have it easier.  I don't think that's necessary.

Hadley: I agree; I don't think that's a W3C thing.  If they need to work out how changes in law are going to change their technologies, that's their business as implementors.   We shouldn't have anything to do with that.

Dan: Is there anything for us to do?

Hadley: Doesn't sound like it.

Lukasz: Monitor.

Lukasz: We can also have the discussion about optional consent in Web APIs.  For example geolocation is sensitive data in terms of GDPR.

Hadley: So we could put an attribute for consent into geolocation?

Lukasz: There's a permissions management API.  There's a prompt to the user.  Why not add an optional message for the purpose of consent?

Hadley: Is this an architecture problem that this group needs to pay attention to?

Hadley: state of permissions API?

Alex: Permissions API being shipped by chrome.  Helps reflect state of permissions added recently.  Being retrofitted to add queryability of older permissions.  Mozilla has blocked prgoress on uniform request API; moving out of the spec to ship independently.

[missed a bit of rapid dialogue between Lukasz and Hadley]

Hadley: not all sensors go thorugh permissions api

Alex: Almost all sensors I can think of now will be reflected through permissions api.  Don't know about vibration.  I'd like to get them all there.

Travis: They'll all be reflected in the permissions API as an enumerated value that can be queried for, at minimum.  At maximum, there's an extensibility thing for adding API surface through the permissions API entry points.  Don't know how propagated that is.  Every so ofter I come across a spec that adds something to PermissionRequest or ???.  Typically model has been API as designed has its own implicit permission model ubilt in.  Act of invoking getUserMedia is its own opportunity for UA to interject permission model.  That feature doesn't have a request entry point in the permission API itself.  Can query with permission API, but can't request access to camera without calling getUserMedia.  But ultimately idea is that API would allow requesting access without calling getUserMedia.

Hadley: Maybe the idea is to...

Lukasz: ???

Hadley: Raise it directly with the permissions API repo.  Point to the relevant bit of GDPR that affects what they're doing, and see how they respond.

Dan: Can we make sure we're creating it in the right repo?  Alex, can you share a link?

Lukasz files [issue](https://github.com/w3c/permissions/issues/169).

Alex: a few concerns.  Many or most browsers will decline to pass page-provided strings to users with requests for capabilities to do something.  We've removed things about alert() or confirm(), and remove developer-provided strings in almost all of our security indicators, because they're not trustworthy.

David: We've had bad experience with page-provided text that's put into browser security-UI messages, because the page-provided text can contradict the browser's text or try to cause the user to ignore it.  So for security we want to avoid having page-provided text in any trusted security UI.

Lukasz: So you'd avoid allowing developers to change the browser UI prompts.

Sangwhan: You mentioned iOS model, but that works because app store apps are reviewed, and you can review the strings as part of that review process.

Lukasz: Alternative would be to provide number of use defined cases to browser vendors, for standardized purposes.  For example, "we collect this data only to display a map".  So users could understand...

Hadley: I think it would be helpful to pull out the bits of GDPR that add this requirement.

Lukasz: There are no clear requirement that geolocation services need to provide purpose; it would only be of help.  I'm not pushing for any solution.

Hadley: I suspect permissions API team don't know why you're saying this.

Alex: GDPR is also European, not universal.

Lukasz: All in the GDPR text can be done by the website itself.  Question is need of whether to translate in a standard browser user interface.

Dan: I'd suggest modifying the issue:  explaining that GDPR is coming and ePrivacy coming later with additional requirements.  Ask if something can be done in the permission API to ask if things can be done in the API to help to meet the requirements.  more specifically, could anything in the permissions API help developers meet the requirements of these regulations.  Then we're framing it as the question of what we can do in the specs to help developers meet their challenges.

Lukasz: Since I brought this permission issue... not a request just an issue for discussion... I'll just enhance it.

Alex: There are arguments that the cookie warning deserves browser UI -- maybe worth a hint to the browser to provide a UI indicator.  That's a reasonable UI feature to add.  I think I'm struggling with what's the equivalent for GDPR.  What's different about a requirement for GDPR-implicated location data versus non-GDPR implicated requests for the same data?

Hadley: GDPR is much broader than the cookie requirement; relates to many more things on the Web.

Dan: Shouldn't be specific to GDPR, but should be informed by what GDPR requires developers to do.  But if there's a way we can help developers develop to the regulation, then that helps things along.  But it shouldn't be "GDPR says this, so the API must do this".

Hadley: Agree... but devils advocate:  I'm for the principles in GDPR, but also for a global web (GDPR is jurisdiction-specific).  There are things in GDPR that go a bit counter to the way things currently operate, like shift in ??? for permissions.  Would challenge some assumptions that developers or browsers have already made about what involvement a user needs.  I suspect that's part of what's behind alex's cuoncerns.

Andrew: Obviously examples like geolocation where information comes from the UA, but there are tons of things that are sensitive under GDPR that are obtained through forms, so site has to take responsibility for GDPR itself.

Hadley: Explicitly asking for information covered by general parts of GDPR, whereas things like geolocation data or fingerprinting or things that users might not think of and lawmakers might not have written in, then there are questions about whether things are protected, so there are specific additional clauses about those technologies.

Andrew: So site would need to put things explicitly on the site about that, but I don't see that as a web platform technology.  It's a coupling of law and transparent behavior from the site owner

Hadley: And punishments if they misbehave.

Lukasz: ???.  Tracking preference expression has dialogs, website can specifically request something.  When extended to others, optionally, not like GDPR would extend to other jurisdictions, it would still be optional to include this kind of text.  On the other hand, there are many users in Europe.  If company provides services to users in Europe, company needs to adapt to GDPR.

Lukasz: We wouldn't sell this as changing specifications due to regulatory requirements, it's just making things more transparent.  Even if it goes in the opposite way of what browsers intend to limit the ability of websites to interfere with standard UI messages.

Hadley: What do we need to do with this.  I don't know that we've come up with any consensus in the group on needed changes to web architecture.

Lukasz: I think there's no consensus here.

Hadley: Should we move on?  Should we leave this discussion open with permissions group.

Lukasz: The issue is filed; let's see what happens.  I'd opt for more transparency; David's take is that there should be less place for web developers to modify standard UI messages.  Whether it's not possible to present text provided by developer that's clearly marked as something coming from website is a different discussion.

Alex: very directly, given user experience research we've done on Chrome, you'll make zero headway with the chrome user experience team.  What I'm trying to say is that user research has shown that users, no matter how clearly it's explained, are not able or willing to make that distinction.  As a result we have a responsibility from a product perspective not to present users with choices they cannot make.

Lukasz: But users still don't understand that access to light sensor or geolocation data might have more consequences.  Take the recent strava thing.  I take the point that users are unable to understand, but ???.    So reasoning here is that it doesn't make sense to specify more information to the user because they will still not understand it.

[ missed a drop ]

Dan: ... discussions that went along with development of Gelocation API.  We should observe and poke, but not be perscriptive about what we think the solution will be, because I don't think we'll find consensus on that point.

Lukasz: just raised an issue, not in dicating anything and not want to expand the discussion to go out of scope of things we're working on, these things are related and this is the only reason we mentioned these. Now move forward

### Publishing WG Activity

Andrew: At TPAC I spent a lot of time in the publication-related groups.  There was one session with a meet-and-greet with web publications and service worker, which turned into questions with Jake Archibald.  It made me realize that there's a big disconnect between the communities.  There are numerous issues opened about manifest, packaging.  They created their own manifest specification, called the readium web publication manifest.  They'e been discussing its relationship to web app manifest, how the lifecycle should work, and how publicatios should be made available offline, and how they should be packaged.  Essentially the problem is that there's so much crossover between these technologies and existing aspects of the web platform that it's unlikely these proposals as currently concieved would be implemented by general purpose browsers.  Might be implemented by special-purpose browsers or e-readers.  So I'd like to give them feedback that we're excited about plugging missing parts of the web platform with book-related things, but we'd strongly encourage them to build on the existing technologies in the platform instead of trying to reinvent them.

Travis: I'd be in favor.

Andrew: If you hit link on readium web publication manifest, they're adding things like metadata object that links to schema.org definition of book, etc., etc. (reads).

Travis: Sound identical to HTMl &lt;link> element relations.

Andrew: spine attribute to jump you to certain points (chapters), and then a collection of resources that bears a frightening resemblence to appcache.

Andrew: So I'd like to say:
> It seems to us that the Readium manifest format is unlikely to be considered for support by implementors of general purpose browsers. Therefore, the question is really, is the goal of this group to make a new packaging format for specialist book reading software and devices, or is it to obtain first class support for missing book-related features in the web platform as a whole?  If the latter, then it is an order of magnitude more likely to be achieved by building atop existing platform features - notably WAM and serviceworker, than creating a separate but similar concept.
> 
> We don't want to be discouraging of efforts or dismissive of concerns around conceptual semantic differences between 'books' and 'web apps', in fact I think your group's work makes us realise that there are clear missing parts of the platform that this work could address.

Peter: Agree we should say something to them as the TAG, to stop reinventing the wheel.  We want them to be here to tell us what needs to be added to the web platform.

Peter: I'd like the point about ??? to be a little stronger.

Sangwhan: Was Web App Manifest around?

Peter: This is recent, last 12 months.

Andrew: There's a long thread about this, issue 32, going back to August.  That's a reopening of an issue from July.  They knew it existed, and have gone and created something new anyway.  The meetings I sat in on, web app manifest came up continuously, because they were comparing what they were doing to it.

Peter: Bear in mind that many of these folks are coming from view that web platform involves XML, semantic web, etc.  They might see what they're doing as using the web.

Travis: Might be implemented in an e-reader.  They might view that as the correct destination.

Andrew: That's why we're asking the question.

Peter: The fact that IDPF merged with W3C suggests the answer to the question tshould be the former rather than the latter.

Andrew: Also want to extend this to ask about packaging.  In some ways it's a less strong point.  Unlike web app manifest and service worker, packaging isn't yet part of the platform.

Peter: And rather than spending effort at defining independent one

David: Might want to talk about packaging more...

Peter: I had a similar conversation with them about JSON for i18n of strings, and should align with i18n WGs documents.

Andrew: I think it's worth mentioning packaging anyway.  Maybe welcome to dial in to our next face-to-face?

Peter: I think we should also raise an olive branch to them, let us know if they're having trouble getting other WGs to address their needs, they can come to us and ask for help.

Andrew: I will revise over lunch and hopefully post this afternoon.

### [Privacy and security checklist](https://www.w3.org/TR/security-privacy-questionnaire/)

dka: we haven't been maintaining this document because we haven't had much expertise in this area. My suggestion is that Lukasz take ownership and that we being working on it more actively. I don't have ideas for new content specifically, but want to get agreement that we should re-start work on this.

[conversation about ownership]

Lukasz: agree it could benefit from some updates. [scribe missed some content]. We can't maintain this in a way that discusses a specific regulatory regeime...

dka: I don't think we need to go through all the issues, but if you agree to edit the document, the process will be similar to other W3C document editing: take input to the document via issues and pull requests and discuss major changes with the TAG.

[discussion of the history of the document and how it has been used in the page, e.g. for Web Payments]

Lukasz: I'm thinking about some short Findings that might go along with the document.

[agreement on work mode]

dka: other thoughts? Are folks OK with us taking this on?

[lack of dissent]

### Design Review Issues

[searching for a specific topic]

### [Accept-CH](https://github.com/w3ctag/design-reviews/issues/206)

Andrew: the latest from Ilya is interesting. In some places it leans on theoretical purity, and in some cases practical reality

Alex: overlap?

Andrew: ...

[discussion of lite vs. full-fat versions of sites]

Andrew: you'll likely switch the JS you send based on what's included in the page, not in the resource itself.

Andrew: Ilya's assertion is that sites will use CH as progressive enhancement...and then everything will be fine.

Travis: but that won't happen in the wild.

Andrew: the argument is that you might not get CH sent if you're in incognito mode (e.g.). So you'll get the "lite" version of CNN in your regular profile but not in incognito. But the breakage is stranger than that: if you go to the first page you get one experience and tap any link then get something radically different. Else you have to have redirects.

Alex: Which is why I'm asking what hte scale of this will be?  You could need a full-fat roundtrip to get to the request that you want in the first place.

...saveData is often a user opt-in.

Travis: How would we envision this being flipped on?

Alex: in Chrome, user choice and we send the header for you if you're on a slow network

[discussion of `Accept-CH` as a general architectural pattern]

Travis: geolocation being an example

Andrew: so that's one thing that's problematic; another is the statelessness argument. Anything that you do in HTTP that depends on previous state seems like a bad call. I know we have some of these already, but it isn't great to add more.

Yves: accept-ch respects statelessness because it doesn't _mandate_ responding with client hints headers

Alex: what's the lifetime of Accept-CH?

Andrew: there's a separate header for that.

Peter: how do servers distinguish this in the redirect case if you don't respond with client hints?

Andrew: you'll have to redirect to another URL. You'll see it happen more and more as we add more client hints. Everyone will want to set these redirects else you won't have any idea what to send.

Yves: we already had this with Accepts headers. People used UA headers instead....

Alex: UA isn't a perfect subsitute. UA tended to correlate with immutable properties of the runtime, which CH attributes don't (e.g. network type, DPR, etc.)

Andrew: we can anticipate bugs. You'll need to use the tuple of UA + CH to understand what's going on.

[we note that this is similar to content negotiation]

Peter: this isn't quite the same, as you have to kick the can down the road to a future request to determine what to actually send. Requiring a second request seems problematic from an architecture perspective. You have to introduce state or redefine what the URL of a "thing" is. If it could be a negotation or if they were always sent, we could sidestep these issues.

[discussion of implementer push-back]

Peter: this breaks URLs. You can't count on a URL pointing to a resource.

Alex: there's an argument that content negotiation breaks the URL/resource relationship, but what's being broken here is slightly different: you break even the relative ability for the same UA/user to get something from a URL.

Andrew: do we want to make a point of following-up on the redirect issue and drop the statelessness issue? If I describe HTTP to someone, I talk about it as stateless. If we're going to add this bi-directional protocol aspect to it...that seems odd.

dka: I don't really see that as a valid objection. What does the HTTP community have to say about it?

Andrew: I raised it with mnot who said some words. If Mark's OK with it, I'm fine with that. We should maybe focus on the indirection thing.

Peter: adding more state seems odd. Where does it end? "With-credentials" on steroids.

[discussion of how to respond]

travis: my concern is responding too late with this and getting things into an inconsistent state where sub-requests ...

[disucssion of timing issues around sub-resource loading]

Andrew: if any sub-resource responds with an Accept-CH, all subsequent sub-resources will get client hints added. YOu might send something markedly different on the first request to the subsequent requests (which were intended for a second page load).

[discussion of joining up CSS DPR w/ network-level information]

Travis: I can imagine other things wanting to reflect similar information; e.g. permissions

Peter: this seems like a giant foot-gun. Many developers will screw this up.

Travis: could we have a generalized verions of this were a developer is able to opt in to specific headers?

Peter: the current version of this is cookies.

Alex: what's different here is the efficiency...

Andrew: ...which is removed by the redirect. There's no value to this if people are going to implement it that way.

Resolution: Alex to respond.

### [ads.txt](https://github.com/w3ctag/design-reviews/issues/201)

Alex: I will ping the thread now

Andrew: Could they respond to the [feedback we raised in September?](https://github.com/w3ctag/design-reviews/issues/201#issuecomment-332172578)

Lukasz: a lot of inconsistencies - incorrect syntax used - some write the file as html. They want something like robots.txt - my main point of interest was transparency side of it for the user since the sites disclose which ad exchanges might be involved in serving ads. They proposed this to fix a specific thing and they wanted it to be simple. 

[Lukasz's Post](https://twitter.com/lukOlejnik/status/959072929744064512)

Hadley: you did research on how many sites used ads.txt

Lukasz: Yes. 12.7% of most popular 100k Alexa sites.

Andrew: I've posted updated concerns against the 1.0.1 doc in the [GH issue](https://github.com/w3ctag/design-reviews/issues/201#issuecomment-362284668) This should be sent to IAB and we should ask them to respond point by point.

Alex: I've asked google people to respond as well to feedback raised in September?

### [ResizeObserver](https://github.com/w3ctag/design-reviews/issues/187)

\[discussion on this issue and how changing sizes of border or padding ...\]

Travis: do resizeobservers notify on CSS animations... use case of a menu and as I pass through them with a mouse the items animate.. would that trigger notifications?

David: I think if they resize then yes.

Travis: antyhing handled by the compositor would not

David: yes

Travis: CSS transitions defines all of that. Do we have any followup comments?

David: \[looks at spec\]

Alex: I had a conversaiton with Alex about which box... his logic was for an implementation convenience it was not inexpensive to get other boxes but it was inexpensive to get \[the one they used\]. ContentRect. 

David: I should look at this in more detail.  Spec has this definition of ContentRect which is weird. I will look at it.

### [Keyboard Lock](https://github.com/w3ctag/design-reviews/issues/192)

closing the issue. Noted that we've seen many lock-flavoured things. Filing an issue on the design guidelines to help guide development of further locking APIs

### [Reporting Observer](https://github.com/w3ctag/design-reviews/issues/195)

swapped the status in, decided to revisit when their open issues from our last discussion are closed

### [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197)

\[Looking at current state\]

David: Someone needs to write a spec. The answer could be that I write a spec for this...

### [Img decoding attirbute](https://github.com/w3ctag/design-reviews/issues/220)

set to extra time ...

Hadley: @jaffathecake helpfully illustrates the problem https://twitter.com/jaffathecake/status/925702096300707842
Sangwhan: for video you could do that (e.g. switch video streas mid watch) with media source extensions 



### [Web Locks API](https://github.com/w3ctag/design-reviews/issues/217)

Andrew: don't like the API shape

Travis: disagree with this feature - don't think we should have a generic locking API

Andrew: choose an arbitrary string and say "lock" and then you have a flag that says you have a lock on it

David: \[question on how to expose in a threadsafe way\] How do you guarantee you don't deadlock.

Peter: no guarantees

Travis: prefer the use cases be addressed by adding features to specific areas where needed... e.g. indexdb?

Peter: this can be used by application level locks - e.g. 2 tabs open to same site can't update... \[meaning bad server application design\]

Andrew: yes - this is the reason why 

Alex: shared workers used by google docs for this - people are doing this by other means right now

Andrew: there are a number of things wrong with this.  it has such a similar use to atomics but atomics can't be used for this because they can't be used across realms. also david's concerns about maintaining the locks. I am concerned about the developer interface.

Travis: \[also these are difficult and this feature would be available to any web developer\]

David: writing threadsafe code is hard

Alex: the reason this proposal is moving forward is that one of the primary use cases for web assembly is high performance games and WASM folks are planning their own threading system - they will be able to lock and deadlock in WASM land... there will be symantic divergence where WASM has superpowers ...  People unhappy with indexdb - i can't mmap a section of a file and do what I want...

David: state of the atomics proposal - in js

Alex: it's in

Travis: we did mitigations for spectre / meltdown for shared array buffers 

Alex: we disabled shared array buffers in c64 - looking to reenable as soon as possible

\[lack of consensus\]

David: if you have stuff based on shared array buffers then you have the primitives...

Peter: you could build the cross tab locking out of indexdb... 

David: I dont think this creates any more ability to block or deadlock the browser than...

Sanghwan: I can see this being useful if you are modifying a cookie for example in 2 different tabs...

\[some further discussion\]

Andrew:

1. should it exist
2. does the api make sense
3. potential browser / stability concerns

Travis: we should be able to explain idb's transaction mdoel using this API

Alex: a good litmus test.

Peter:  extra time

### [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198)

Alex: Think we should ask to ping us when it has matured a bit more

### [Gesture Delegation](https://github.com/w3ctag/design-reviews/issues/199)

\[...reviewing...\]

Peter: no comon framework for describing these similar things - can haz primitives please?

... e.g. a way to manage some kind of generic state that could be passed between parents and frames.. as uopposed to building in user interaction as a new thing. Is there a way we can build a mechanism to propogate state generically?

Dan: some of these thingd have different security considerations

Peter: could we have the same primitives at least even if we don't expose it...

Travis: when the user interacts that state gets flipped... In te code handling media playback you check that state. The pieces missing are: exposure of that state, ability to read and write it, building blocks of playing media what would need to check that info...  It's a tall order.

Peter: this notion - that you don't get to autoplay a video until user has inetracted - that is just something to try to mitigate user annoyance - should it be baked into the platform before we understand / have more experience. If we had the primitives to experiment with these sorts of thigs... e.g. interactive state should be reflected as a pseudoclass in CSS...

Travis: we suggested modeling this as a permission.

Peter: yes.

Travis: Ian should describe why he took the direction he did.

**END OF DAY TWO**

**TUNE IN TOMORROW FOR THE EXCITING CONCLUSION**
