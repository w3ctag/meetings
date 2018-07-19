## TAG Teleconference
##### 17 July 2018

Present: Travis, Dan, Kenneth, Peter, Lukasz, Hadley, David, Sangwhan, Yves, Alex

Chair: Peter

Scribeinator: Dan

---

Agenda:

* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - @cynthia @dbaron @travisleithead

Travis: multiple rounds of feedback about shape and form etc...

David: multiple versions...

[reviewing what the right version is...]

David: .. some more work to do...

Peter: put off to f2f?

David: probably.

Peter: bumped to f2f.

* [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231) - @slightlyoff @dbaron @hadleybeeman

David: went through theirt feedback - they have not responded in last 24 hours - we should give them a chance to respond.

Travis: [inaudible]

Peter: milestone?

David: f2f

* [CSS Selectors 4, :focus-visible](https://github.com/w3ctag/design-reviews/issues/233) - @dbaron @travisleithead @plinss

Peter: pending?

Travis: pending external feedack...

David: looks like the PR was closed 2 days ago

Alex: I will chase Rob.

David: they closed the PR without merging it...

David: new issue (PR) - 2897 - which is open... [link?]

Travis: is that different?

David: it's just an issue.. I think we're waiting on movement here.

Alex: What's necessary per CSS working group?

David: One of the editors need to be ok - Tab & Elika

Travis: they're adding some examples and giving more detail...  We can weigh in on discussion in 2897... we could be hands off...

Alex: Tab said he could give this PR a look.

Peter: should we keep this open?  

Alex: can we revisit next week?

Peter: Ok - we're review at the f2f.

* [Notification Inline Replies](https://github.com/w3ctag/design-reviews/issues/284) - @torgo @hadleybeeman

Hadley: when we last left this I was concerned about the phishing potential - Anita made some changes ...
... I went back, was concerned where the text is going.  They've replied they can't have control over that.

Alex: any time an origin is able to run code they can do all of these things.

Hadley: i fel like it's conceptually different in a notification but may not be relevant. I think the feature makes sense... Our usual response is to put it in the spec - and to put concerns in a note. It would be great if she could add it to the explainer. I wanted to know: how do we deal with non-normative notes for whatwg... 

Alex: same way - we cna ask for it.

HAdley: I suggest this is way to proceed.

Lukasz: I am happy with the updating of privacy consideations and they filled out the security & privacy questionnaire.

Alex: I'd like to flag - the set of avenues for locking this down look very narrow. One way to do it could be to have certain user agents that want this feature use CSP etc... 

Lukasz: additional permissions request...? 

Alex: I don't know how to make it understandable to the user.

Alex: e.g. [channeling hadley] I have to type stuff into the notification response and who knows where it goes?

Hadley: [missed it]

Alex: we do attribute these notifications with an origin. Because we promote the origin model... maybe we should encourage UAs to promote origins in the UI.

Hadley: how is this different from what she's written already - suggesting the source be visible.

Alex: not different.

Alex: any notification clicked or dismissed could ... exciltrating analytics or intent is possible.

Hadley: I feel like the stakes are different to putting in text...  Risks are high.

Alex: do we have an enumeration of mitigations- what USas should think about - e.g. trustworthy sites should be able to do this...

Lukasz: secure transport... identify the target - use of https -  if the user has been asked permission - click a checkbox..

dka: I think this ties into upcoming workshop on permissions and user consent. One of the things we've thought about was that often you have websites gaming or abusing permissions. Alex, you've talked about the Chrome model of site trustworthiness

Alex: So, we do engagement. "If you use example.com a lot, we could grant it more..."  Persistence and installation are also factors. We are also looking into crowd consent -- if almost no one believes this is example.com, we wuldn't want to let it do bad things.

dka: Until now we've talked about secure contexts. Notion: insecure web and secure web. Now, the default assumption is everything is secure.

...Where do we go from here? An enhanced secure context that could be generalised enough to let UAs make their own definition of what is in scope but is specific encough for a spec to have a normative reference to it? "In this spec, this feature should only be availble to trusted sites" etc.

Alex: imagine that you had a set of other things you'd like to request along with it - the user agent could have a policy to figure out whether it trusts ... creating the policy enforcement ... the 

Lukasz: non-deterministic reasoning?

Alex: yes  we have that already... for example - the ability to be installed ... that gates things like storage durability... also bad behavour we want to remove...

Lukasz: we are already going in that drection... safari...

dka: discussion at the face to face?

Hadley: i will respond to anita directly and propose this concern end up as a non-normative note 

Peter: go ahead an close after

Hadley: OK

Alex: i will update the TAG from our security team about this bigger issue

* [CSP feature 'unsafe-hashes'](https://github.com/w3ctag/design-reviews/issues/291) - @cynthia @travisleithead

Travis: i looked at this with Sangwhan - for a lot of legacy web sites it may not be feasible for them to apply a directive like - externalise their event handlers... they may have an onclick handler they depend on...  they also don't want to resort to 

Sangwhan: unsafe inline is pretty terrible

Travis: that's a little too much - this is a midddle ground where they specify a hash - of a particular block of script. as the parser runs throuhg the document it encournters event handlers.  Seems OK. Risks that an attacker that an attacker can know what you want to allow trough.   

Sangwhan: My understanding was that this is limited to handlers ...  

Lukasz: it's also about styling; a possible "concern" when a lot of inline functins - say 1000 functions  - http header would be too small.  That would be an unlikely scenario though.  

Travis: it could lead to having a lot of bloat in your CSP file

Alex: what is actually being hashed?

Lukasz: for example, function names (i.e. hash("meow()") )

Sangwhan: for externalizing the scripts you have inline 

Alex: lexical analysis?

San

---



