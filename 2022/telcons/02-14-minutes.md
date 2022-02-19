# TAG Minutes for week-of-14-feb-2022

## Agendas

### Breakout A (Europe / US) - [2022-02-14](https://www.timeanddate.com/worldclock/converter.html?iso=20220214T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo
* [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @atanassov
* [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @torgo, @kenchris, @hadleybeeman
* [Broadening the user base of WebAuthn](https://github.com/w3ctag/design-reviews/issues/686) - @torgo, @rhiaro, @hadleybeeman, @plinss, @atanassov
* [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [[css-values-4] The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov

### Breakout B (US / APAC) - [2022-02-15](https://www.timeanddate.com/worldclock/converter.html?iso=20220215T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @LeaVerou, @atanassov
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov
* [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/704) - @hober, @atanassov
* [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov


### Breakout C (APAC / Europe) - [2022-02-15](https://www.timeanddate.com/worldclock/converter.html?iso=20220215T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
* [SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov
* [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov
* [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @torgo, @kenchris
* [Web App Launch Handler](https://github.com/w3ctag/design-reviews/issues/683) - @kenchris, @hadleybeeman
* [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon
* [HIDDevice forget()](https://github.com/w3ctag/design-reviews/issues/703) - @cynthia, @torgo
* [Region Capture](https://github.com/w3ctag/design-reviews/issues/710) - @cynthia, @torgo
* [Review request for Confirmation of Action API](https://github.com/w3ctag/design-reviews/issues/713) - @torgo, @rhiaro


### Plenary Session - [2022-02-16](https://www.timeanddate.com/worldclock/converter.html?iso=20220216T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Special session with members of the AB to get a briefing on legal entity progress

* Decision on F2F?
* Breakout Rollup
* Issue Triage

## Minutes

### Breakout A (Europe / US) - [2022-02-14](https://www.timeanddate.com/worldclock/converter.html?iso=20220214T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Peter, Tess, Yves, Lea, Hadley, Rossen
Regrets:

#### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo

Dan: we were on the verge of closing it.. then we got some comments. Mozilla's position shifted, and it will be shipping. Response that they took feedback into account. Does not require browser to expose more entropy. Then a long comment from Jo Rabin of 51degrees, kind of rehashing a lot of the issues raised on the initial thread on 'the previous issue](https://github.com/w3ctag/design-reviews/issues/467) about the first announcement of this.. These have been addressed as far as I'm concerned. But Jo is pointing out this is not really being standardised at ietf or w3c, just sitting in wicg. Recent comment about "market is not ready", "wholesale disruption", "significant disfunction". I think Mike Taylor thinks they have addressed these concerns.

Yves: we just have to figure out if it's a sound proposal or not

Dan: There may be a reasonable request here, but not sure if it's for the TAG. I want to ask Mike to address the issues Jo has raised.

Tess: that sounds good. We should do a bit more than pass the buck to Mike. Things already addressed - maybe we could add a comment that calls out some of those things and point to PRs/etc? And ask Mike to answer others.

Dan: where did Mike point us to when they were talking about response to community feedback? We got Mike on a call and he presented this... Not the things in response to the Mozilla comments, but in response to previous 51degrees feedback. Around the how partial is partial issue. How much of the UA string would remain.

Tess: conversation on #467.. 

Dan: [the call where Mike talked to us about this](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/06-14-minutes.md#ua-cleint-hints).. 

```
Hi Jo - Regarding some of the issues you raised I believe Mike and Yoav believe that these have been addressed - see the
[minutes of our call on 14-Jun from last year](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/06-14-minutes.md#ua-cleint-hints).  
@Yoav can you provide any further detail or comment here?
```

Dan: we'll keep it in play for this week

Hadley: we have enough evidence in EWP - Priority of consti.. etc... to defend [closing].

#### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @atanassov

Dan: no feedback from requester. I can raise with Chris H tomorrow.

#### [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @torgo, @kenchris, @hadleybeeman

Peter: I'm satisfied with Ian's response. Concerned about how it will evolve, but they're on the right path to evolve in the right direction. Depends how fast banks and payment processes catch up and that industry is slow, but they're doing what they need to do.

Dan: Ian responded in the affirmative to my privacy related question. I think that wraps this up and we should [close]

Rossen: and the conversation between Ian and cypherphone?

Dan: it's a conversation for them to manage..

Rossen: that it will carry on in the respective WG

Dan: Proposed closing comment:
```
Hi @ianbjacobs - thanks for all the great responses and engagement. The TAG is happy to close this review positively. 
I hope our feedback has been useful. I hope that further conversation on the additional issues raised here can be carried 
on in the appropriate working group forum.
```

**closed**

#### [Broadening the user base of WebAuthn](https://github.com/w3ctag/design-reviews/issues/686) - @torgo, @rhiaro, @hadleybeeman, @plinss, @atanassov

Hadley: they repsonded to a bunch of things. They're opening a bunch of security issues that they don't want to spec out but that they should raise so implementers consider them. They have accepted that and opened an issue of their own on it so I'm happy. But there's other stuff in there.

Rossen: doesn't seem like they've addressed Peter's comment

Peter: more of a suggestion for an alternative approach, not necessarily our job to redesign their features for them

Rossen: is this something we care strongly about to wait for them to get back to us?

Peter: general concerns that if they go to a model where keys are entirely software based, I agree this will make the feature more useful and more people will adopt it, and as soon as there's a major breach the trust will be burned down to the ground.

Dan: worth articulating

Peter: I suggested a hybrid approach... hardware keys would take longer to catch on. My comment isn't a blocker.

Dan: Useful for Hadley to leave the sentence about the thread .. and on this basis happy to close

Hadley: okay

#### [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo

Tess: Peter raised the point that it's weird they're combining properties and values, media features and values, in the keys. Their response is basically about keeping structure simple, less nesting. I don't think the latter falls from the former. If I'm writing code the difference between Peter's suggestion and what they have is a quesitno of where you end the string and where you put the brackets. From a dev perspective they're equally simple. 

Rossen: from an extensibility point of view..

Tess: also broadly equivalent.. Preference for less nesting feels like a personal preference of the feature designers as opposed to something justified on simplicity grounds, because I don't think it's any simpler. It's valid, but doesn't strike me as the strongest argument

Peter: if i want to iterate through all the colours chemes specified I need to start parsing keys

Tess: great followup point, that's why they're not the same

Rossen: my reaction too. Jamming in values along with the attributes of properties in this case syntactically, Tess, I agree with what you said. You could put them in the same line or space them with new lines and braces. But dark and light and everything else that's gonna come up are values of that property we all know so combining them together leads to all kinds of residiual issues like the one Peter pointed out. Stronger arguement to put them on a separate level

Tess: worth replying ot the last comment pointing out that they didn't take your point that iterating over these would require parsing keys and in the other design it wouldn't. That's absent from their reply.

Peter: on the other side, I do reall having this conversation before about something else in th emanifest and they took the same appraoch. So if there's consistentcy..

Tess: cnsistency on the platform is nice when we manage to pull it off. Overall there is lots of inconsistency. All things being equial, consistency is nice, but in this case there's a real downside to this design that you've identified. Might be worth not being consistent with other bad things.

Peter: perpetuating a bad pattern

Tess: I can leave feedback, these aren't interchangeable for that reason

Dan: Lea has left a couple of comments in the meantime. Also while we were speaking my computer has turned to dark mode and github has gone from light to dark.

Lea: comment I left was not immediately related to this discussion. They said it's already definable through CSS - what are they referring to? Custom properties for theme colours? SOmething I don't know about? Assuming it is definable through CSS why would we duplicate it into a different API? What if you could link to a stylesheet that defines these very eseential things that you want a splash screen to have access to before the app loads. Takes an extra request, but so do other things in the manifest like icons.

Tess: linking to a css file from the manifest would mean that the manifest parser would have to have a css parser in it .. big ask

Lea: true. Fair enough. Down the line, what if we need to duplicate more CSS in the manifest?

Tess: oh yeah, your worry is very well-placed

Rossen: yoru point is generally speaking something I agree with. We had this conversation about how much of the platform you expose to the manifest and end up duplicating. But from the app packaging point of view it's been a hard argument to come around on either side. Not the hill we want to die on.

Lea: agreed. I can edit to add the part about the CSS parser.

Tess: need to take some time to write a comment

#### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Lea: I don't see anything wrong with it, seems uncontroversial, reasonable media query addition

Rossen: from privacy point of view? Exposing the fact that you're ..

Lea: doesn't specify how it's set - automatically or user preference? Left up to implementations

Rossen: if you're roaming and you have to pay and you don't want to the devie can be aware and say reduce the data and it's going to propagate down to the UA. That makes sense

Lea: the OS itself could expose a setting so the user could explicitly opt in or out

Dan: they haven't really written a proper response to the privacy and security questionnaire. Simply pointed us to an issue which has a link to the [privacy considerations section of the spec](https://wicg.github.io/savedata/#privacy-considerations)..  but no answer to questions...

Lea: no proper explainer...

Rossen: explainer is a link to an issue in the CSS WG

Hadley: a closed issue

Dan: privacy considerations section is minimal to say the least. We should ask for proper consideration of privacy qustionnaire.

Tess: the reason you write an explainer isn't because the TAG wants you to, it's for everyone. We might be who nag about writing them but it's really for a general audience to understand your feature, a background. 

Dan: I do think they should spend time thinking about the issues raised in the questionnaire. Pointing to a random link where they'v ebeen discussing privacy shows they're dismissive of this bieng a privacy issue. We should hold off responding

Amy: questionnaire is to prompt them to think through important issues and report back. We might miss things from a surface level review

Lea: [writes comment]

#### [[css-values-4] The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov

Rossen: zero engagement since last time

Dan: will discuss with Chris H

Hadley: is this all Google or are there other implementers? Only see Google mentioned on the issue.

Tess: not all Google, engagement from our side, not sure who from Mozilla

### Breakout B (US / APAC) - [2022-02-15](https://www.timeanddate.com/worldclock/converter.html?iso=20220215T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Max, Peter, Rossen, Sangwhan
Regrets: Lea

#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @LeaVerou, @atanassov

Rossen: The issue has been evolved into a rework of the proposed feature. We're closing this review and encauraging the authors to repoen/open a new one once ready.

#### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Lea asked to defer

#### [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov

Concers about feature detection don't seem to be answered, propose closing with concerns at plenary to give Lea/Tess a change to have input.

#### [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/704) - @hober, @atanassov

Closed satisfied, but with concerns about abuse from adtech.

#### [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov

Punting to next week


### Breakout C (APAC / Europe) - [2022-02-15](https://www.timeanddate.com/worldclock/converter.html?iso=20220215T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Sangwhan
Regrets: Amy

#### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman

#### [SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov

#### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov

#### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @torgo, @kenchris

Dan: ken left a comment... no response so far...

**assigns Sangwhan**

Dan: this is about JavaScript performance.  Explainer does not define the user need ...  

Sangwhan: provenance - it's from a non-browser org...  so this makes sense.  Presumably they want to capture traces & profiles at the end user level instead of having to capture with devtools?

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/682#issuecomment-1040037009)

#### [Web App Launch Handler](https://github.com/w3ctag/design-reviews/issues/683) - @kenchris, @hadleybeeman

**re-assigned and put on agenda for next week**

Dan: Looks like they have raised at least one issue based on our feecback so far.

#### [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon

Yves: it's a way to set http headers from a server response - it's not possible in http to make claims on "this other resource".. faking server-header replies for this particular site.. it's dangerous - not clean architecturally - it may change and you have rotten content configuration... it may be conflicting with what the server may reply at some point. If people want to have an optimised way to figure out that the 3rd party server would like to have a UA platform version client hint sent in the upcoming request - it shouldn't be in the markup of another web site. It should be in something that might be cached - e.g. hsts. You could do the same here - for this particular subtree of site send us the UA platform version client hint... The server has to be configured .. the client (browser) should cache that information.

... if the intent is to say "the remote server cannot be configured properly" then you wouldn't need client hints because you wouldn't be able to handle them anyway.

Yves: **leaves comment**

#### [HIDDevice forget()](https://github.com/w3ctag/design-reviews/issues/703) - @cynthia, @torgo

**agreed to close**

#### [Region Capture](https://github.com/w3ctag/design-reviews/issues/710) - @cynthia, @torgo

Sangwhan: miscommunication in Elad's response to my comment... i meant a box like a real box.. if the elemnt changes dimensions then you're changing size of box...  

Dan: something something user need... complexity .. and what (possibly simpler) alternatives were considered?

Sangwhan: let me get in contact with Elad.

#### [Review request for Confirmation of Action API](https://github.com/w3ctag/design-reviews/issues/713) - @torgo, @rhiaro

Dan: this starts off with user need which is great.

Dan: Regarding the privacy & security questions - do we think it should be restricted to secure contexts?

Sangwhan: given how easy it is to get https certs not sure it will mitigate against misuse.  The other part that concerns me - 

Dan: shouldn't this be the same bar as push notification API?

Sangwhan: gate it behind a permission?

Dan: I don't see the argument ...

Sangwhan: not convinced that it makes it less dangerous .. i won't lose sleep.  

[...side discussion on secure contexts...]

Sangwhan: I'm more concerned about will applications be too chatty?  other potential issue - aria so far has been declarartive - this is an API that changes that paradigm... 

Dan: it's in the AOM work - so associated with other technologies that do the same...

```
Hi @sartang - thanks for this really well-written explainer! We especially appreciate how it starts with the user needs.   Do you have any further info on multi-stakeholder interest?   Have they had feedback from the ARIA community on this?
```

*Dan & Sangwhan to have side discussions*

### Plenary Session - [2022-02-16](https://www.timeanddate.com/worldclock/converter.html?iso=20220216T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Rossen, Yves, Dan, Hadley, Peter, Lea

Guests: Léonie, Tzviya, Eric, Dave, Chris

#### Special session with members of the AB to get a briefing on legal entity progress

Tzviya: We as individuals, more than AB reps, decided it's time to share more information. We've reached out to a few groups, we want to get facts out there. 

Chris: We wanted to start by what we're doing. W3C was started at the beginning as an agreement between a dept at MIT and two (eventually three) other organisations. It doesn't exist as a single legal entity. Over time this has become less effective. Director is less involved, steering committee is less involved, and there is no oversight and no coordination between the sites other than the programmes they choose to do themselves. We have four entities now that operate largely independently. Formal objections are delegated to the team, which makes the escalation path less credible. MIT has decided they want to end their hosting relationship. Now is a good time.

Léonie: question for us as a community: what is going to change for us day to day? in one sense, not much at all. We'll carry on producing technical standards. Members will retain rights, capabilities and responsibilities they already have. A few things will change, for example the council. How we replace Tim once he's officially gone. 

Other thing: our erlationship with the hosts will change. one possibility: some/all will continue in a partnership. Chris mentioned MIT are keen to check out, but Beihang and Kaio are keen to carry on. We'll also have a board of directors to provide a governance/oversight. we haven't had much of that and will come with a successful legal entity.

Dave: current status: governance and funding. we've been working thorugh governance,funding and operational issues with the steering committee for a couple years. They are loath to give up control of hte organisation, but show no initiative in solving these problems.

The steering committee recently agreed that the board of directors will be member-majority. Still working on teh detail

We need a way to fund the legal entity. Costs are constant, income is variable. And we need an operational reserve to adjust to changes of income. 3 possible routes: hosts have provided some, but will cover legal, filing fees and startup costs. ISOC have indicated they may be willing to provide funding, but want to see a member-led consortium and want to match money coming from the membership. We've talked to some potential sponsors, but some are concerned about the lack of track record of being prudently run and needed a bailout 10 years ago. Remote potential of some sort of EU fujnding in Europe, but we're unaware of the timing or strings attached.

We need to work out the long term relationship we'll have with the hosts. We don't have a good model yet.

Eric: What are the possible outcomes? We think there are four:

1. We make no progress and at the end of the fiscal year, MIT would end the hosting agreement without new structure in place. Most likely they would pass on their hosting position to maybe the W3C Inc, which is a shell. Jeff is the only board director there. We think this is the worst case scenario. Don't think any of hte existing hosts or Jeff would be motivated to solve the governance issue.

2. Everything remains status quo. MIT might cave, feeling guilty about pushing W3C out without funding. Or they may move their hosting rights to another host. This doesn't solve the governance issue - there would be more drawn-out negotiation and more work for us to find a permanent solution.

3. The W3C might get funding from the EU. Thee not been very transparent on what they want for that funding, but I think we can anticipate that there would be strings attached, and it would be more EU-centric. We don't know what this woudl look like.

4. A new legal entity led by member-majority board, likely co-funded by ISOC and volunteer members, replacing MIT's role and some or all of the other hosts transitioning to a partnership agreement. This option has been stalled. We came up with it last year but haven't made progress, due to politics, preconceptions, etc.,  With respect to funding, some companies are worried about negative PR if they volunteer to help.

Tzviya: all decisions have to be run through the Steering committee today: the SC is the representatives of four hosts, plus Tim and Jeff. AB are advisory, and can't make any decisions. 

We need to find an acceptable solution for many stakeholders. WE need to get support from hosts, members, etc. to go forward.

We need a clear communciations plan, and we need to eliminate uncertainty across all stakeholders.

This is causing a lot of anxiety among staff, whose jobs are dependent.

There is the potential of an economic downturn, which could result in lower membership and less funds.

What can you do? For TAG... working in councils is helping. Helping us with comms. Insisintg on transparency, for example at AC meetings. Irt shouldn't be a surprise that MIT is pulling out. The situation with ERCIM.... 
And we'd like yur support for a member-driven organisation. That worked for a long time and isn't working right now.

W3C Inc isn't necessarily a for-profit organisation. Looking at different us-based versions for not-for-profit.

Dan: What is creating the blockage toward the option to create a non-profit organisation?

Chris: A move to any of these structures will need funding, and changes in governance. Right now, the hosts are responsible for the money side, for better or worse: They own the bank accounts, receive the funds, pay the staff, etc. If a lot of members drop out and we run short on payroll, those hosts cover that.

Dan: considering that MIT has taken a lot of money from W3C members over hte years, they aren't willing to put up mone yto seed fund this?

Chris: they likely are, but it may not be enough.

Also, we need agreement on governance; right now, MIT own the selection of the Director and CEO.

Tzviya: each host has a different relationship with W3C. MIT are hands off, but Kaio have a close relationship. Hosts make money out of this, and so we're trying to make a plan that keeps good relationshisp with partners. 

Now we're meeting monthly with the steering committee. In 2020, it didn't meet. We can't progress this without them.
W3M and the AB were working on this separately, and now they're working together.

David: we're not making progress because the W3C has a decision-making structure that hasn't adapted to the current reality: Director is not engaged, we have a steering committee who didn't meet for an entire year and are not engaged at an operational level, and haven't shown a sign of being pro-active. 

We tried to form an interim board, consisitng of the members and steering committee, and they said no.

Léonie: in the past six years, there has been action to galvanise governance, funding, etc. And it has been frustrating. AB has put togheter plan after plan to get all the stakeholders together. We all have a vested interest in this future. 

Rossen: Many things... since you've been close to the receiving end on a lot of those conversations. A couple of things are not computing. We had a few opening statements to cement that nothing is going to change. I want to believe that, that technical work is going to happen, decisions continue to be made in the same fashion. That is not true because people will get into arguments and there will be escalations and formal objections and this is when we get closer to the top, and currently it seems like the top doesn't work at all. Regardless of what happens, if there's no good governance I do not believe in that opening statement which is that everything is going to be the same. 

Another thing - from everything I'm teasing out and going back to conversations I had with Jeff 4 years ago, when he was trying to pitch the new structure, it doesn't look like much has changed since then. I'm curious, is the leadership of this new entitiy more or less assumed, and the rest of the management and stuff that is going to be part of this effort, or not? Is this mostly a formal renaming? Or would thre be a lot more to it?

Dave: re: 'not much will change' - assuming we succeed in a LE with stable goernance and unified management, all the visions we've seen with the structure and board of directors should have no effect on the technical program itself. The board would not approve publication or WGs. That would be in the hands of the AC and WGs. That's what we mean by we expect the technical work to continue unchanged. Modulo 'if' we succeed in forming stable management. Which we have not yet succeeded in.

Eric: One of the biggest shocks for me on the AB 3 years ago to help with the spin out and raise money was eventually I discovered that with the exception of MIT none of the three other hosts are motivated to give up their control of their respective organisations. We were misled, intentionally or unintentially, that the steering comimttee had approved spin off, if we raise the money we can spin out. That is the fundamental problem that we're running into. Especially ERCIM, they need the money to continue to exist. Kaio will continue to exist as a university, so will Beihang and MIT, but ERCIM is in a sense an existential issue for them. It's really hard to get to a solution because the people in charge right now are not willing to give up their control.

Tzviya: to make sure we're separating the concepts of director-free and legal entity. Director free, which includes FOs, is an attempt to make sure what's happening with things like resolving FOs and how charters get approved, which is more clerical work for the most part, reflects what we want the organisation to be. Right now FOs are very rarely looked at by the Director (Tim) but for the most part they are handled by Ralph or Philippe. We could continue that way, but they won't be around forever. One thing we discover is that w3c relies on a lot of single points of failure. Council is an approach to avoidng that. That is apart from the legal entity. Whether the legal entity changes the way we work on technical standards, the director-free aspect has nothing to do with it. One thing we need to work on when we're communicating thi sis avoiding letting our frustrations get the better of us. We've done a huge amount of work on this. It has been a frustating process. We've been told over and over again our solutions aren't good enough. We're attempting to build processes and write docs about how the w3c can exist as a standalone legal entity, and every detail is picked at. What we'd like to convey is we're attempting to build processes so the w3c can continue to thrive. We could really use the support of the membership in moving this forward. Experience with fundraising, with forming this kind of organisation, with convincing people to budget, we could use expertise or general support.

Hadley: I would be happy to help. I think .. I heard your frustration and I think it's importatn that you have somewhere to put that. You need to be able to keep going. Don't feel bad about that. I'm struggling to see if there's a right answer. Laying out those 4 options, I can see that 4 is the best answer, I'm behind that. In terms of how we get everyone to that point. Do you as a group see a way through this? Are you saying we need to push harder and hope? Tactics and strategy - a sense of how to get from here to there?

Dave: we currently engage in a "triumph of hope over experience" - we're giving it one more try but many structural problems remain. The AB finds this intensley frustrating. We can't actually make any decisions, only advise. Those who could make decisions seem unwilling.

Leonie: Beihang and Kaio have stepped up to be part of the task forces working on these things. Angel is cochairing a task force with Tzviya. That is a welcome step.

Dan: If the other hosts are undermotivated to move to a new legal entity, has the option of MIT stepping back but the other three hosts carrying the ball been floated? Separating the discussion and timeline about the LE from the fact that MIT is stepping bac? 

Leonie: it would likely be logisticaly impossible even if the other hosts were willing. China has to tread gently with employing people from overseas in their academic institutes. Setting up a w3c china could take 2-3 years to put into place. ERCIM isn't talking to us about any agreements, not extending the current one.

Dan: I don't understand that, and the other statement that ERCIM want to continue their relationship with w3c. Surely they know that this apocaplyptic event is coming and if they don't do something they won't have any w3c at all?

Dave: the host agreement between MIT and ERCIM is supposed to be renewed a year in advance of its expiry. Last summer they were negotiating the one that expired at the end of 2021, MIT offered the contract, but ERCIM didn't sign. MIT has offered an extension, and ERCIM haven't signed that either. 

Tzviya: the AB has been trying to get w3m to do something about the ERCIM situation in particular. Jeff frequently tells us we should draft an AB proposal resolution to try to get the SC moving. Getting our voices together, AB and TAG together, all of the elected officials, not sure what to convey but we need to express our discontent. I don't know exactly what but this has to move forward. If the SC hears from all of us that we need to advance the LE on this timeline, it might make a difference.

Eric: the situation that MIT is much more complicated. We've tossed around ideas of how we might be able to negotiate with MIT to take over their position as the lead host which then makes it easier to facilitate the spin off with the other hosts, but unfortunately the dynamics are quite complicated. MIT you have Tim and Jeff, and their own agenda, MIT does want to get out but they are also very conerned about potential negative PR if they leave w3c too early. 

Tzviya: I think we have agreement on writing some sort of statement, I don't know it would have any effect. 

#### Decision on F2F?

#### Possible reschedule for breakout B?

#### Breakout Highlights

#### Issue Triage
