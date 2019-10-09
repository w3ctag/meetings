## TAG Teleconference
##### 09 October 2019

Present: Kenneth, Peter, Tess, Dan, Yves

Regrets: David, Sangwhan, Lukasz, Alice

Scribe: Kenneth

---

Agenda:

* Miniapps statement
* Update on any outputs from TPAC
* Update on AB process questions
* Update on any work progress on automation tasks

Stuff assigned for today:
* [Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406) - @hober, @hadleybeeman
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman

Stuff that had no milestone but also said in progress:
* [Service Worker Pattern Matching](https://github.com/w3ctag/design-reviews/issues/417) - Kenneth, Sangwhan, Dan
* [Storage Corruption](https://github.com/w3ctag/design-reviews/issues/419) - Kenneth, David, Sangwhan


---

### Miniapps statement 

Dan: Sangwhan wants to make a more official mini app statement from the TAG

Dan: I will turn it into a blog post and maybe link to the TPAC session on mini apps which is public - this is the TAG statement of mini apps

Dan: I have read the statement through again and again and I believe we stand by it

### Update on any outputs from TPAC

Dan: Any update?

###  [Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406) - @hober, @hadleybeeman

Tess: We talked about this last week on the call, without having seen the [minutes from the TPAC session](https://lists.w3.org/Archives/Public/public-editing-tf/2019Oct/0004.html), have since read these minutes

Tess: I did a very short summary of what I saw on slack the other day, basically, Gecko and WebKit engineers expressed concerns about the security/privacy implications of the API. And as a follow up I was trying to figure out if there was a Moz standards position on this, but there wasn't so I filed one.

Tess: The minutes were quite sparse so I would like to get a bit more info. I will make sure there is a link to the moz standards position issue from the TAG issue.

Dan: What are the main issues?

Tess: Main issue is security - the concern is that allowing web sites to write arbitrary typed concent to the paste board exposes the native apps to untrusted data that could lead to /sandbox escape/ to native apps.

Tess: One possible migiration is to expose the type of what is exposed, so that native apps by default wont read such data unless explicitly opting in. That seemed to be preferred by most people present, but doesn't work for integrating with existing apps that may never be updated.

Tess: [Anne said](https://github.com/mozilla/standards-positions/issues/206#issuecomment-539435685) that there had been some concensus the previous TPAC on a different solution that in my opinion sounded more promising.

Tess: One possible mitigation is instead of making it being opt in, would be to put writing to the paste board a permission prompt - but the opposition is that it is difficult explaining that to users.

Tess: I hope that Hadley has also looked at the minutes

Dan: Coming back to this I feel like that these issues have been raised before (looking at explainer) - the security issues are important what what I am most converned about is the notion that the user might have something on their clipboard that is privacy infringing (like password) and then some use switches tab and suddently a web page get access to this. Think about Slack for instance, like for me it has access to a lot, so switching to it might show an prompt.   

Dan: I don't see this handled in the explainer - is that already a possibility with async clipboard? Why isn't this mentioned?

Ken: Can you add to the issue? 

Dan: Yes, I can make that commen

### [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman


### [Service Worker Pattern Matching](https://github.com/w3ctag/design-reviews/issues/417) - Kenneth, Sangwhan, Dan

Kenneth: no further progress since TPAC.

[we agreed to close this issue for now]

### [Storage Corruption](https://github.com/w3ctag/design-reviews/issues/419) - Kenneth, David, Sangwhan

Kenneth: kind of the same... lots of feedback from TPAC... some people think we should do something different... 


