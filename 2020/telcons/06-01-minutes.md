## TAG F2F Plenary
##### 02 June 2020

---

Present: Dan, David, Alice, Peter, Tess, Rossen

Regrets: Sangwhan, Kenneth, Hadley

### Agenda:

### Plenary Session - [2020-06-03](https://www.timeanddate.com/worldclock/converter.html?iso=20200603T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* review from f2f
* [s&p questionnaire pull request](https://github.com/w3ctag/security-questionnaire/pull/81)
* land PRs on [design principles](https://github.com/w3ctag/design-principles/pulls)
* [miniapp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478)
* Issue Triage

### PRs in design principles

#### [unsafe in names](https://github.com/w3ctag/design-principles/pull/193)

[approved, after changing invariant to guarantee]

#### [priority of constituencies](https://github.com/w3ctag/design-principles/pull/204)

[approved]

David might try to propose further changes if he can think of how to word them

#### [APIs to features](https://github.com/w3ctag/design-principles/pull/207)

Alice: Feature is an abstract term - API is the surface exposed to developer.

Rossen: guidance we provide to people should be about naming of the APIs, not naming of the features...  I think we need to be careful about this - looks half-and-half ready.

Peter: there's a lot of places where I defaulted to feature as I didn;t have an alternartive. Didn't want this to just be about "JavaScript API" -   maybe we need a section that says "in this document when we say API we mean..."  or use a better term....

Alice: apart from the naming section, I think Feature works everywhere else. But maybe just for naming we can revert to saying API and consider a follow-up PR for "what we mean by API".

Peter: fine

Dan: I'm Ok with that

Peter: Features can be broader.

Rossen: you are talking about APIs in some places...

Peter: if we're going to use APIs to mean something beyond javascript APIs then we need to be more specific in ...   I will revert the changes in the naming section.

Alice: I'm happy to approve conditionally.

Dan: yeah .

[S&P Questionnaire PR](https://github.com/w3ctag/security-questionnaire/pull/81)

Tess: this just changes it to use github actions ... fewer moving parts, etc... just works.  I have tested. David has looked and approved.

Peter: lgtm

David: the one thing is it depends in another repo....

Tess: it depends on 3 other repos - it's how github actions works - you use pre-canned recipes - there are several recipes for deploying a static page to the gh-pages branch.  I filed an issue for bikeshed to add this. So when that happens it will have fewer dependencies.

... i think this is ready. But I want to hold off until tomorrow morning local time to merge it.

Peter: [suggest using the curl method]

Dan: please let Yves know and then we can republish the doc to TR space

Tess: Ok

Tess: another change I made - there was a historical file of original questions. I wrote a script that extracts the current questions from the bikeshed document and generates the markdown - so you can copy and paste into an explainer to answer the questions.  Does it make sense to link to it from the note saying - if you want to answer these questions in an explainer, go grab this text.  or... auto-add the text to the explainer explainer...

https://github.com/w3ctag/security-questionnaire/blob/master/questionnaire.markdown

Dan: I think it should be a link from the explainer explainer and a link from the issue template.

Alice: we've been saying for a while we need to make this easier to fill out.

#### Miniapp URLs - 

[Bumped to next week]

#### Scheduling a Retrospective session

Scheduled for 2nd plenary slot today

what worked, what didn't work...

David: we might want to consider - more time or changing frequency...

Alice: .. spreading out over multiple weeks?  

### Plenary Part 2 : Retro of f2f

Present: Peter, Rossen, Alice, Tess, Dan, David

#### What Worked, What Didn't Work, What we would want to do differently

Rossen: the one thing that didn't work well was the time between sessions - 3 to 4 hours - wasn just enough time to take me back into regular work, which wasn't great.

Alice: I told my team I was off that week.

Rossen: having the dedicated 3 days back-to-back - with dedicated meeting times - was great. That helped me focus on TAG stuff only.

Alice: due to timezones that wasn't an option...

David: everyone's day was the same but offset by one hour...
... problem with spreading slots per week is that we can't move issues backwards.

Peter: maybe a-b-c per week? 

Dan: i already feel like we did 2 weeks

Alice: don't agree - the f2f week was much more exhausting

Dan: We could try spreading it out more...

Peter: we could do more of a time break between sessions...

David: we could think about what happens if we spread - instead of every 8 hours, every 16 hours. That means each person would have 1 session per day, but it alternates between morning and afternoon.  .. to get same amount of time we would have to go into following week...

Peter: or longer sessions

Rossen: if we make the sessions 3 instead of 2 - 

Alice: and shorter sessions?

Tess: 6 hours per day feels like a max...

Peter: but 16 hours between sessions - more breakouts per sessions - less hours per day.

Tess: 4 hours per day instead of 6.

Peter: I've been wanted to work on tooling

Dan: Andrew did a script for breakouts... we could adopt that.

Tess: tooling improvements always great... but manual improvements shouldn't be gated...

Tess: we should  consider process improvements that we can execute manually and then we can write a script...

Alice: any suggestions

Dan: we should think about it in terms of hours per day.,...

Peter: for me, taking a day off costs money...

David: with 16 hour gaps we can fit 7 in a week - so we could do 6....

Eur/Asia C Monday  
NA/Asia B Monday/Tuesday  
Eur/NA A Tuesday  
Eur/Asia C Wednesday  
NA/Asia B Wednesday/Thursday  
Eur/NA A Thursday  
Eur/Asia C Friday  (??)

Eur/NA A Monday  
Eur/Asia C Tuesday  
NA/Asia B Tuesday/Wednesday  
Eur/NA A Wednesday  
Eur/Asia C Thursday  
NA/Asia B Thursday/Friday  
Eur/NA A Friday  (??)

times: 7:00-11:00 and 15:00-19:00 (UK/California/Seattle/Japan) or 8:00-12:00 and 16:00-20:00 (CEST/Sydney)

David: if we wanted to go to 4 hour slots we could push it a half hour on each end...  Time zone math changes in sept, oct, nov....

Rossen: sounds like it'll take 3 or 4 hours at least a day for that entire week.  It gives a much better way to organize the rest of your day... 

[Other issues:  what about the "blank" sessions?]

Alice: seems like alternating would be disorienting... 

Peter: 6 4-hour slots vs 9 3-hour slots  

Dan: thinking about the "unscheduled slots" we could explicitly assign unassigned people to those slots.

Tess: [on comparative to other F2Fs] some of the differences are because we are a group that is small and we do almost exclusively breakouts.  ... amount of time in 2 chunk - CSS did 4 chunks over 2 weeks... we did breaks well relative to other groups...  given our distributuon I felt was good scheduling. 

Alice: the one on one breakouts are really effective... 

[discussion on breakouts vs plenary]

David: the thing about a group plenary - difficult to fit in

Alice: also with time zone differences - if we want everyone to go to one thing we can't have it more than an hour.

David: in January the plenary is easier and the breakouts become harder.

Rossen: (1) feel like for next one I need to be "out out".  (2) in terms of productivity it was productive - other major difference with TAG is that there is no lack of issues... couple of sessions unscheduled... +1 to the read-outs. 

Peter: ditto

Alice: as far as scheduling breakouts - yes it was difficult and tedious but it needed to get done.

Dan: i think the process is good but we could apply some more automation.

Rossen: if we had the automation that would do a first pass - non-controversial ones, 2 assignees only, group those together, that would help.

