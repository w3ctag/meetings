## TAG Teleconference
##### 04 September 2019

Present: Kenneth, Peter, Tess, Dan, David, Alice, Sangwhan, Yves

Regrets: Lukasz

Scribe: Dan

---

Agenda:

* [Rendering Independent Scroll Offsets](https://github.com/w3ctag/design-reviews/issues/409) - @alice, @dbaron
* [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @torgo
* [More restrictive hasEnrolledInstrument() for autofill data](https://github.com/w3ctag/design-reviews/issues/407) - @dbaron
* [Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406) - @hober, @hadleybeeman
* [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @alice, @torgo
* [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @dbaron
* [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @dbaron
* [Prefetch request changes to improve privacy](https://github.com/w3ctag/design-reviews/issues/398) - @lknik
* [Same-Origin iframe document-access limiting Feature Policy](https://github.com/w3ctag/design-reviews/issues/397) - @hober, @lknik
* [WebRTC-SVC](https://github.com/w3ctag/design-reviews/issues/396) - @cynthia, @kenchris
* [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393) - @alice, @dbaron, @lknik
* [Scroll To Text](https://github.com/w3ctag/design-reviews/issues/392) - @hober, @alice, @dbaron
* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon
* [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385) - @hober, @alice, @kenchris
* [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris
* [Portals](https://github.com/w3ctag/design-reviews/issues/331) - @hober, @cynthia, @dbaron, @kenchris, @plinss
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @hadleybeeman, @plinss

---

Logistics for next week:

Alice: Meet at 8am to have breakfast at Mori Tower?  With one group going around 8:30?

Peter: AB members will also join us

Dan: Florian, Thursday at 10:00

Tess: Elika may also be available to join.

Ken: Project fugu meeting also overlaps with us.  They are discussing things like native filesystem, etc...

Dan: I'm also working on putting the open issues together in a spreadsheet for us.


#### [Rendering Independent Scroll Offsets](https://github.com/w3ctag/design-reviews/issues/409) - @alice, @dbaron

Alice: no spec changes but they want feedback on what we think about it.  Take it to a breakout?  10am/5pm thursday/friday?

#### [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @torgo

Dan: I will work on this before the f2f

#### [More restrictive hasEnrolledInstrument() for autofill data](https://github.com/w3ctag/design-reviews/issues/407) - @dbaron

Peter: Waiting for feedback?

David: yeah it woudl be good to get an answer to the question I asked.

#### [Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406) - @hober, @hadleybeeman

Tess: the main security concern I have is that this a new way of exposing untrusted data (from the pasteboard)... In the answer to the questionnaire, they had a great answer to "what should this questionnaire have asked" - which was "does this spec compromise the user's system?" Their proposed mitigation is to put a permissiomn prompt over it. I don't think this is adaquate.  People will just say yes because they won't understand the security implications. I'd like to see a more serious mitigation.

David: I agree that is not the sort of question you can explain to a user coherently.

Dan: this is a real dangerous thing because all kinds of info in the clipboard - private info - links, passwords, email addresses, etc...

David: we've always considered the ability to read from the clipboard without an explicit paste gesture to be a security veunerability.

Tess: Dan, why don't you and I each capture our concerns in the issue.

Dan: yes.

Dan: [case where safari prompts with a 2fa code to paste it in]

Tess: in the safari example, the web site doesn't see the 2fa code until the user makes an action to submit it. 

[bumped a few weeks and we can pull it into f2f if appropriate]

#### [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @alice, @torgo

Alice: I had a look at that.  I left a long comment. I haven't had a look at Brandon's comment.  How webxr works with feature policy - i don't have context. Can someone else take it?  Brandon explained the relationship with webvr and asking us for feedback on use of feature policy....  

Dan: I would say yes, otherwise the data leaks through the webxr API then it could be used by e.g. trackers.

Alice: does blocking these features amount to blocking webxr when webxr exposes these features - or is it up to the developer to know "webxr exposes these features therefore I'll block webxr via feature policy"?

David: there are various options - if webxr might depend on a feature then you act as though it's always required...  

Alice: device orientation?

David: You could say: if the feature policy says you're not allowed to use device orientation, then webxr doesn't work, even on a desktop device.

Alice: so you don't get the inconsistency.

Alice: the suggestion: if it depends on it in any context then access in all contexts should be restricted.

Dan: I can get on their agenda at TPAC about it?

Alice: 3 options ?  2 options ? 2.5 options: (1) if an API which webxr depends on on this platform is blocked then block webxr (1a) if an api which webxr depends on on any platform then block webxr on any platform (2) up to the developer to sepataely block webxr.

Dan: Did you make the big PR and did they comment?

Alice: I did send it in. They said thanks but they won't have time to think about it. I wrote a chunk on accessibility.  It raises a question also relevant to Toast thing. In both cases there needs to be work done to come up with an accessibility story for the space. History of HTML - ARIA came much later.... How much do we want to require a coherent a11y strategy before allowing it onto the platform? Comments I had: what scope is there to develop that story - are we limiting the options?

Dan: Of note: https://www.w3.org/2019/08/inclusive-xr-workshop/ - workshop happening in November.

Alice: to what extent are the core xr team doing that work? or at least on top of that work?

Dan: I confirmed one of the chairs will be there but don't know about the rest of the core team.

[bumped to tpac]

#### [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @dbaron

Tess: I gathered internal feedback and will write it up.

[bump to f2f]

#### [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @dbaron

[bump to f2f]

#### [Prefetch request changes to improve privacy](https://github.com/w3ctag/design-reviews/issues/398) - @lknik

[bump]

#### [Same-Origin iframe document-access limiting Feature Policy](https://github.com/w3ctag/design-reviews/issues/397) - @hober, @lknik

[bump]

#### [WebRTC-SVC](https://github.com/w3ctag/design-reviews/issues/396) - @cynthia, @kenchris

Sangwhan: I briefly looked at it. SVC stands for scalable video coding.

[scheduled to breakout at f2f]

#### [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393) - @alice, @dbaron, @lknik

Alice: I filed a couple of issues.

David: Alice & I filed some issues. A response came in 14 hours ago.

Alice: In terms of granularity - made a good poont that the cumulative score is what is meaningful. Exposing the raw score with developer guidance is what needs to happen.

David: their responss to comments seem reasonable.

David: should this be in webperf?

Dan: can we close it?

David: I'm OK closing it. Just typing up a comment that it would be useful to have guidance in the spec?  We can lgtm and close it.

#### [Scroll To Text](https://github.com/w3ctag/design-reviews/issues/392) - @hober, @alice, @dbaron

David: we did talk about it last week...

Tess: yes, we did talk about it... 

David: we struggled to draw conclusions.  I was gonna go ask Anne what the right forum for talking about URL changes is. Anne got back to me.  I haven't proxied that response yet.

David: one of the underlying question is "who are you supposed to talk to about fundamental changes for URLs"...  [So difficulties] but at the same time it seems like a decent idea.

Peter: bump to TPAC?  There might be more people involved with URLs.

Alice: do we have a good dislation of the things we're struggling with about it?

David: one thing is: if you are going to change URL syntax who do you need to socialize it with?

Alice: so, yes the design seems OK but wer'ee not sure about changing URL syntax.

Peter: for me i have concerns that micro-syntax is overloading fragment identifiers... everything is stepping on everything else...

David: that's why they are coming up with this new mechanism for a piece of the URL that is not expose to the site so it doesn't conflict with another thing.

Peter: but is this already being used by some sites...

Alice: yves points out that fragments need to be interpreted 

David: it's a little more backwards compatable by using ## 

Dan: We are kind of defenders of the URL.

Peter: f2f before tpac?

* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon
* [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385) - @hober, @alice, @kenchris
* [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris
* [Portals](https://github.com/w3ctag/design-reviews/issues/331) - @hober, @cynthia, @dbaron, @kenchris, @plinss
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @hadleybeeman, @plinss