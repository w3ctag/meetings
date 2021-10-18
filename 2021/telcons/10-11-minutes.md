# TAG Teleconference
#### 11-13 October 2021

---

## Agenda:

### Breakout C (APAC / Europe) - [2021-10-12](https://www.timeanddate.com/worldclock/converter.html?iso=20211012T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou, @kenchris
* [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
* [Pre-CR review of CSS Cascading and Inheritance Level 5](https://github.com/w3ctag/design-reviews/issues/678) - @torgo, @rhiaro


* [Media Source Extensions](https://github.com/w3ctag/design-reviews/issues/576) - @cynthia

### Plenary Session - [2021-10-13](https://www.timeanddate.com/worldclock/converter.html?iso=20211013T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
* [Private Network Access (aka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @ylafon, @hadleybeeman, @plinss
* [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia
* [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov
* [WebTransport review request](https://github.com/w3ctag/design-reviews/issues/669) - @plinss, @atanassov
* [Auto-expanding details elements](https://github.com/w3ctag/design-reviews/issues/677) - @hober, @LeaVerou, @rhiaro, @kenchris

* Breakout Rollup
* Issue Triage

-----


## Breakout C

Present: Dan, Ken, Yves, Sangwhan, Amy, Lea, Hadley

Regrets:


### [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou, @kenchris

Ken: not much has happened yet, someone else is taking over. Should be restarting the discussios at tpac. Bump it.


### [Pre-CR review of CSS Cascading and Inheritance Level 5](https://github.com/w3ctag/design-reviews/issues/678) - @torgo, @rhiaro

### [Media Source Extensions](https://github.com/w3ctag/design-reviews/issues/576) - @cynthia

Sangwhan: I think we LGTM'd this

Dan: it says resolution satisfied, but the last comment by Sangwhan was asking a question, wiht a reply, and no followup response. And it's not closed.

Sangwhan: we looked during f2f. [reads] The final verdict was we have questions and concerns but not a strong preference for either. There are two options for doing this, one is obviosuly doing domain specific promises and generic promises.. if they can't sketch otu the time to do byte based promises we shouldn't block that work, it's a big chunk they need to do and enforcing that is not fair. It was a question about what would be the path forward given these two options. They answered, I'm going through the comments. Bottom line is: it's fine.

Dan: we should close it

Sangwhan: doing it

**closed**

### [Auto-expanding details elements](https://github.com/w3ctag/design-reviews/issues/677) - @hober, @LeaVerou, @rhiaro, @kenchris

Lea: seems like a reasonable feature but there are accessibility considerations, there's a [linked thread from mozilla standards position](https://github.com/mozilla/standards-positions/issues/578) that talks about it

Dan: they don't say it's harmful. Not sure what Anne means about dashboard entry

Lea: looks like there are no a11y concerns, just discussion of implications, but nothing problematic. I don't see anything against it.

Dan: filled out security & privacy 

Lea: already in html spec..

Dan: in the s&p questionnaire there is a find in page vulnerability.. there's a mitigation being implemented in chrome. Worth mentioning that we'd like to see what impact that has, or we support the proposed mitigation. Worth noting they've considered this. Is it documented anywhere? If it's an addition to the html spec it doesn't seem to be documented anywhere other than the explainer. Is there security and privacy considerations in html?

Lea: there are in individual parts of the html spec

Dan: [writes comment] Any other questions/comments?

Lea: do you think the question would block the review?

Dan: I don't think so, not blocking

Lea: if we post a comment saying it looks good and add proposed close they might not get to your question.

Dan: maybe we can close at plenary or next week

Sangwhan: it can be used to tell what user is searching for, problematic?

Amy: they link to a demo of that in s&p

Dan: could be problematic

Sangwhan: possible through an indirect channel..

Dan: is the user expectation that what they're searching for in an article is private to them?

Sangwhan: huge meta question here, I'm not sure. The query string can be referred to so what the user was looking for in a given webpage can be inferred by the referrer which contains the query string from a search engine (google removes that), except when you have scrolltotextfragment enabled when you can infer to some level. I don't really know the implications.

Dan: should we ask privacy ig to weigh in?

## Plenary Session

Present: Dan, Rossen, Peter, Sangwhan, Kenneth, Hadley, Yves, Lea, Amy

Regrets: 

### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou

Lea: not sure I understand the use case

Kenneth: you have a lot of .. rendering today virtual scrolling - now you can do search in page - and you know that yiu're going to render soon. It's a way to request rendering...

Lea: for pre-rendering of subtrees.

Rossen: It's the oppososite of pre-rendering. not rendering as much as possible - but being ready to paint... There are many different ways you can scroll something into view or close to the view... ways to understand when something is close to the visible viewport... everything else from API point of view is not supposed to be effected. Where things come into friction is to do with accessibility.  A different view on top of DOM.  Not the same as the render view.  In order to complete the correct view .. you need info ready.  With this technique in fact some web pages that are too large to hold with a screen reader... this approach will help because you're now reducing the amount of info that goes to the screen reader.  Where I pushed back on this - and opened up a design principle issue (new features shouldn't rbeak existing ones) if you want to enumerate all the headings in a doc you can do this today regardless if the heading is visible or not - but here that promise is broken. Things can be parsed but not ready for the accessibility ... So it's a game of trades... Fine line is - how much of a bennefit vs the accessibility risks... We've come a long way in the discussions in various places... The current proposal is mostly there - one remaining issue which is pertaining to one particular value - that still has open discussion. The rest of it .. worked out. It's beneficial to users of regular media as well as those using assistive tech.  Grealy improves experience from CPU, memory PoV. 

Lea: Why is this a HTML attribute and not a CSS property?

Rossen: we had a long discussion and took it out of CSS and that was feedback that came partially from TAG at the time... It was a CSS wg decision after a [long conversation](). 

Ken: that would be great to know... people will ask.

Peter: sounds like the feature can defer computation of style... 

Ken: right and now you can set the priority - that's good for battery performance UX.

Peter: but if you're not computing style on the unrendered content then it can't be a CSS property.  At some point the parent will be the root...  

Lea: defering rendering doesn't mean necessarilly defering parsing of CSS...

Peter: you don't have to compute style if you know e.g. it's off-screen. You can say "i want to compute the login controls first and the ads last". 

Lea: since you have to parse stylesheets anyway...

Peter: you do have to parse but you don't have to match selectors. Seperate computation than parsing the stylesheet.  HTML attribute can say "deprioritize this".

Lea: but if you don't compute the selectors...

Peter: if it was a CSS property then you'd have to do the selector matching - that's why it's an attribute.

[some discussion on this point]

Lea: another question - how are authors supposed to use it? Are you supposed to set it on elements or change it when you want it to render?

Ken: you set it beforehand.

Rossen: right.

Ken: but for web components - it would be annoying to have to set this for every element...

Peter: you don't have to set it for everything - this is something you "set and forget".

Ken: in some cases for components you need to set it in many places...

Dan: who is intended to use this? I'm hearing adding complexity to the web platform for a marginal nanosecond gains in performance?

Ken: the display login teams.. web components.. working on small features on the web that you can build web components, scroll in list, find in page, that are going to be really fast. They dont' expect everyone to do their own. If it's not something everyone is going to do and use these componants it's going to be super fast. Have an API that they set globally for every componant of that type. Instead of putting it on the devs using the custom element

Peter: I hear you but not sufficient. Just because an element is used for certain types of things doesn't tell you how it's being used. A custom input could be used for two different things in one page

Ken: change the default.. you can change it if you know what you're doing

Peter: that's reasonable

Lea: how does this attribute behave when nested?  render priority user blocking.. 

Peter: good question - you can increase priority down the tree but increasing priority gets weird?

Dan: what is stopping someone providing third party content through an api (eg. an ad) from saying my ads are the most high priority thing? From hijacking?

Ken: very good point

Lea: also share Dan's concerns about adding complexity with nanoseconcds. Not clear to me the perf gain. Nanoseconds, miliseconds? On a sufficiently large app, what kind of gains?

Peter: I'm thinking about huge pages, understand where it could be seconds


### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman

Dan: k provided [a respoonse](https://github.com/w3ctag/design-reviews/issues/342#issuecomment-932526615)...

Hadley: [ua policy](https://github.com/privacycg/first-party-sets/blob/main/ua_policy_proposal.md) doc is thorough - I'm getting closer to seeing what she's trying to accomplish - establiisng a definition of web site... that's making more sense. I'm still concerned about the abuse potential. She outlines an independent enforcement entity - i'd like to know who this is and how they're funded and what their motivations are - and does it cover the entire web?  I'm thinking how much of this is for the western developd world - and further fragments the web.  Is the web just a complex and ongoing software project for large companies.  We shouldn't sleepwalk into that.

Amy: I also read the UA policy and had similar thoughts.  Still a contradiction - K says a site can be in only one set - and in the policy doc it says...  "site authors may choose to form multiple first party sets" - they are using domains and sites to mean different things. 

Hadley: I highlighted that we need to talk about that. e.g. Google as owners of google.com, google.co.uk - and youtube as owner of youtube.com, youtube.co.uk..  but both under the same parent company

Amy: domains can't be in more than one set.

Sangwhan: all the google properties will be in one set...?

Amy: it'd be helpful to have a use case for that explained.. One party can participate in multiple sets with different domains.  

Dan: facebook have a whole bunch of domains associated with facebook and a whole bunch associated with whatsapp. The way they're using this is all the fb domains are in one fps and all the whatsapp ones ar ein another fps, but technically it's the same party because they're both facebook. The party of facebook can have multiple sets.

Hadley: we should ask k to flesh that out.

Amy: what's the legal data question - if one party can put different domains in different sets there are data sharing issues...  e.g. facebook has facebook.com domain and it's in a set with some other advertizers ... whatsapp with a different set of advertizers.. can data flow between those?

Peter: it seems like a legal & regulatory restriction.. you couldn't restrict it technically...

Amy: a couple of other things... i thought the stuff about implementing the UI surface in the browser sounds really good. If the browser surfaces it to the user... but I have the impression we can't standardize UI... 

Hadley: we do sometimes put hints in ...

Amy: it seemed like we can't have normative text on this... 

Peter: i don't think we can't have normative text - if there's a compelling argument spec could say it.

Amy: how testable is it?

Dan: we have reviewed lately apis normative text around notifications. W'ere not telling the browser how to raise the notification but we are saying they msut have a permission request. APIS that say you must ask the users permission.

Ken: apis just have the hook.. then you can always say yes, doesn't actually have to add the prompt

Amy: they suggested popups as a potential solution - didn't sound like a good direction.  and that same quote about parent company owner/operator. that might not be applicable internationally, and might not be future proof wrt company structure.

Hadley: some people use parent companis to hide things... hide ownership ...  there was a big issue in the press in the UK about companies not paying substantial tax...   construct of trying to identify the parent company is not necessarilly helpful. 

Amy: also not necesarilly useful to the end user - if the end user isn't familair with the parent company becaue they only know a particular brand...

Hadley: also: i wonder - if we were approach with cookies and cookies didn't exist would we push back?

Dan: yes knowing what we know now.

Sanghwan: yes many things...

Amy: will draft a response to the UA policy stuff ...   I will run through k's other responses as well.


### [Private Network Access (aka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @ylafon, @hadleybeeman, @plinss

Yves: not much since my last commet.  We gave feedback we need to care about older devices.  We could give feedback that the rest is ok but this point is sitll pending. 

Dan: closed as satisfied with concerns?

Yves: yes we should express concerns.

Peter: do we have issues open in their repo? I'd feel more comfortable closing this if we had them.

Yves: I'll check it.

Peter: after doing that then close and comment with satisifed-with-concerns.

### [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov

Dan: still blocked on FPS discussion

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov

### [WebTransport review request](https://github.com/w3ctag/design-reviews/issues/669) - @plinss, @atanassov



### Breakout Rollup

#### Breakout C

### Issue Triage



