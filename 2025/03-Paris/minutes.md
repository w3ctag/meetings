# <abbr title="Technical Architecture Group">TAG</abbr> Minutes - March 2025 <abbr title="Face-to-face">F2F</abbr>

* Present: Amy, Dan, Hadley, Jeffrey<!--, Lea-->, Lola, Marcos, Martin, Matthew<!--, Max-->, Peter, Sarven, Tess, Tristan, Xiaocheng, Yves
* Regrets: 
* Scribe: Amy

## Architecture of the Web ([slides](https://docs.google.com/presentation/u/0/d/1JNHUnDlnwCDbQAFc8SHdAM--cbC943XaYyCz3oxxHSE/edit))

Jeffrey: what is the architecture? We've learned a bunch since that document was written. I don't think we should update the document. Volume 1 was designed, aimed at programmers. First priority is not programmers. What if we look at the arch from their point of view? A lot emerged because nobody was thinking about it when the web was designed. THought of a bunch of pillars of what stuff exists in emereant architecture.

... Access

... Discovery. Original vision was people would follow hyperlinks. Go to adjacent websites. Search emerged as random access way of getting what you wanted. Nobody designed that in.

... Authoring. Expected, but details not. Tim thought it would be in browsers but it's in web apps.

... Funding was not anticipated at all. Advertising the primary way it happens right now.

... Governance. Some bits was expected, mostly standards bodies. Civil governments also have a role to play. 

... Other aspects to brainstorm (later).

... Nobody has been managing this, thinking about it holistically. Some problems. Authoring is centralised and inaccessible to the average person. Transition to apps - hard to archive things without unique urls.

... Bad ways of figuring otu whether a website is trustworthy.

... A lot of privacy problems, that there is already a lot of focus on. Other people are handling this.

... User attention is being overexploited. No systematic way for people top ush back on that. Websites are being exploited (AI is the most obvious example). Funding is centralised. All of the infrastructure bits are funded by google. Not resilient. Too many monopolies -> enshittification. Governance is not coordinated. Standards bodies and regulators have started talking to each other ut there's a lot more to do.

... the way standards bodies are funded and get participants is biased towards people who have spare time.

... How can we start thinking about this? The first thing we started wrt architectural problems was the commons research.

... Summary of what kinds of problems thinking about web as a commons answers:

... how can end users manage and improve the supply of websites? Websites manage and improve supply of visitors? Collective governance institutions.

... Infrastructure lens. Robin wrote a lot about this.

... Important to look at what we can affect. Instead of complaining that things are bad... think about what do we have the leverage to nudge?

... What do we want to discuss more right now? Should we write something new about architecture? If so, what? What should we do next on the two angles that we've already talked about that might have a way of improving some of this commons and infrastructure problems?

Hadley: describe where we are now, so we have a common vocabulary

Dan: focus on the "So what" - the actionable advice that we give to things in flight in w3c because of this thinking.

Jeffrey: what's next for commons work?

Dan: stream of work on sustanability, societal impacts. How does this relate to that? What can we draw out of commons discussion to help us in those?

Jeffrey: one of the pillars could be connections to the real world

Martin: how the incentives align to create the system that we have

Dan: kind of agree we don't need to focus on privacy, we have privacy principles. HOwever don't think it means we shouldn't work on privacy or should stop thinking about privacy. Just that we have a body of work.

Jeffrey: yes. Follow through, but we don't need to do new stuff.

Martin: may be new stuff we haven't covered yet. Shouldn't be rehashing.

Matthew: whilst learning about commons, was there anything you came across that really goes against something we've previously put in a finding or a principle?

Jeffrey: nothing comes to mind of us contradicting best practices. We have a bunch of blind spots.

Matthew: we should talk about gaps then?

Marcos: reminds me of times the TAG oversteps its boundaries in some ways... eg. societal stuff gets difficult. Don't know how many of us are trained sociologists. We risk entering into areas we shouldn't without having proper training. Should be mindful of when we know the area. It's a global thing.

Peter: the nature of the architectural choices shapes the societal impact of the web. A lot of the original design of the web was designed around specific societal goals, which were not being met. It is encumbant on us to see what went wrong. Use the alignment between the architecture of the web and how it impacts on people.

Dan: should we record what societal goals have not been met as part of this discussion?

Lola: original goals of the web are good but also that was a really long time ago so I wouldn't want us to use that as a set of rules to go by. Things have moved very rapidly since then. I do think it can be used as a guide. We can speak to the spirit of the thing rather than using it as a checklist.

Peter: yeah. It was one man's opinion. Lots of room for improvement. We can't take a viewpoint that technology is not political and there is no societal impact.

Jeffrey: having an idea of the goals we want the web to accomplish might be useful.

Dan: balancing act that we tried to do with EWP. Wade into an area that some might have seen as far afield from what TAG should be working on but doing so in a way that provided a foundation for the other work we're doing.

Tess: EWP is a good example of doing what Marcos is talking about. WE rely on the work of ethicists and domain experts to distill that into how does this apply to the web. But we weren't inventing ethics from first principles.

Xioacheng: +1 to goals

Jeffrey: suggest focus on 'so what' and what we have leverage over.

Hadley: governments... trying to figure out what they should regulate, what the right answer is for the role of goverment. A number ar elooking for a helpful right answer. I'm in a position of trying to explain 'this is how the web should work and therefore' pay attention to privacy, spam... don't go in and regulate the standards. There's nothing written that says this is how the web works and therefore accept this as the starting point from which to figure out how to regulate. I think that would be helpful.

Martin: I've heard "don't regulate standards" a number of times. I want to challenge that. 

Yves: what does it mean regulate standards?

Martin: right

Yves: take WCAG.. has been endorsed. Didn't impose something on the standard itself. But enforced it on people

Martin: this happens all the time

Yves: that's one way of doing regulation. The other way would be "we need this standard to do this thing" which would be a different thing.

Martin: that's why I want to ask that question. It hink there are answers that would ilicit a negative reaction. We need to put that in the light.

Hadley: I'm okay with that

Martin: in the middle of a world that has been created by private entities essentially operating without any sort of oversight and governance. Maybe protecting them by saying "don't regulate standards" is maybe not the most responsible thing to do.

Hadley: shorthand for there's enough stuff to pay attention that it's easier to focus on all the behaviours from a policy and regulation perspective than focus on standards. WCAG good counterexample. The EU continually suggesting to replace cookie banners with something in the browser could be great... and that's to do with standards. But it's another discussion.

... Descrption of what the thing is. In our world that's how things work, not "regulators please do this"

Martin: shocking lack of understanding about how things work. Eg. I was at a workshop a few weeks ago with people asking all sorts of questions and assuming how things work: why don't you just turn off cookies then? Had to explain that the market dynamics in the browser industry.. that's not something people understand.

Tess: "deep linking" rules as if that's something bad.

Hadley: in the UK there's an organised lobbying group of advertisers who have a specific idea of how the web works which may include things not everyone agrees on

Lola: why is there a lack of understanding? Is it documentation is out of date? Not widely shared?

Hadley: all of that

Marcos: not just about documentation...

Lola: Martin gave an example of academics don't understand a thing.. along with the technology there should be some kind of explanation..

Marcos: we document use cases but... cookies is an interesting one.. dynamics were market driven, but also we need a way of storing sessions... we don't know what we don't know.

Dan: Standards and governments - helped to create the UK gov open standards policy. Defines open standards, open venue, avaialble for free, ideally royalty free etc. In doing that I learned a lot about the ecosystem of international standards, ISO standards, how governments generally speaking interact with those orgs. Huge ecosystem that we don't really engage with at all ... do we want to talk about that? What is it that we're talkinga bout when we talk about standards and governments.

Jeffrey: would add to Lola's list - the documentation a lot of time doesn't exist. It takes a lot of work and nobody is doing that work. 

Amy: and a lot is interdisciplinary

Jeffrey: maybe we're the only group who could pull some of that together

Martin: some folks at ietf also have done that work

Jeffrey: to add to "so what"... w3c is an industry consortium. Commons research is about participants governing themselves. We could kick that off - take members of w3c and help them coordinate to address many of Robin's infrastructure areas. One that comes to mind is the way that search works .. relies on clickstream data to optimise search results. That's an obvious potential commons and nobody is sharing that data. Even small search providers. W3C could help with that. A bunch of other areas that we could find potential commons that are currently owned by a signle company, but if we organise second place and down in an industry to aggregate that often works.

Amy: something to do with adtech here too..

Jeffrey: IAB has some standards that act as a commons

Martin: exists to be exploitative

Jeffrey: could extend that to some other parts of the industry

Dan: you had something about managing visitors as a resource. HOw can we turn that on its head and think about visitors as a constituency, thinking about making things great for visitors. Who are people. HOw can we build it all from their perspective instead of from the sites that want to manage the visitors.

Martin: Tragedy of the commons in the sense that an individual website has no incentive to treat their visitors well but if other websites treat their vistors poorly your website suffers by virtue of being adjacent. If they were to collectively decide to set a minimum standard of how we treat our visitors the experience for all of them collectively would improve. That's the nature of what we can look at. That is net positive for visitors.

Jeffrey: would add that a commons exists when you don't have a regulator telling you what to do. Asking industry to work together to improve its treatment of is visitors is a voluntary standards thing. If the visitors get together and try to force industry to behave better, that's a government regulation. We can do both but they take different approaches.

Dan: if visitors come together to force a better commons structure isn't that collective action? If they tell the government to that's governance...

Jeffrey: existing commons metaphor is derived from natural resources so doesn't have that possibility. Having visitors come together to boycott or force regulation is a reasonable path but it isn't commons work it's something else.

Lola: there are cases where users are organising among them selves when a service changes - eg Firefox, or X. 

Jeffrey: not sure it's a commons question. A book [Exit, Voice, and Loyalty](https://en.wikipedia.org/wiki/Exit,_Voice,_and_Loyalty) about when an institution starts declining. THe people involved in that institution have two options. Exit - switch institutions. Or use their voice and try to fix the institution they have. Those two kind of compete and work with each other but there are prconditions for either of them to work. For exit to work you have to have other options. If Firefox starts having trouble and was already the most ethical of the browsers, where can anyone go? We're less clear on what the preconditiosn for voice are. People need to be able to express themselves to the organisation that's doing bad and have a reason for them to listen.

Martin: I understand why changes were made and people were annoyed. Exit is not always an option. 

Dan: "so what" list is not very actionable. Would love to leave with at least one candidate design principle that comes out of the discussion we're having about the commons. Want some actionable guidance.. could a finding.. or a response to a design review.. that helps us move our collective work in a certain direction.

Hadley: helpful scene setting. Propose we come back to the question.. keep it in mind for the rest of the 3 days and come back to it in the last session.

Jeffrey: makes sense. Also: not sure this level of architecture is going to produce direct action on design principles. So far apart in the scale. Architecture should tell us what standards to build. Standards involve particular details and design principles talk about those details.

Martin: agree

Jeffrey: not optimistic it'll all apply..

Dan: still feel like there must be something in the web is a commons, the web must operate in a particular way, therefore this, therefore that, therefore when you're designing the next webrtc feature you must keep this in mind

Jeffrey: it's a good hope..

Matthew: i agree it would be nice but can't see yet how we would do that. Really obvious thing - it seems only the TAG can describe how it is at this point. One of the things about regulators is I don't think we should be telling people what to do. THe way that we could improve the whole situation is by educating people as to how things work. If we're seeing huge gaps in that and we don't think we could offload that work onto some other group, I think that's really important. Challenge is time and resources. Seems clearly needs to be done.

Lola: kind of disagree that we shouldn't be telling people what to do. I think we should. The W3C "we", guided by not just the TAG but other groups too. Using accessibility as an example is a clear telling people what to do so people can use the web in a way that is safe and accessible for them. When I think about the peopl ewho are being harmed the most by the current web they need someone to tell browsers and others what to do so that they can use the web in a way that's safe for them.

Hadley: Agree with both. Somebody needs to tell people what to do. They won't always do it. Agree a lot of value in writing things down, and describing , not least because the discovery mechanisms and the funding stuff has at times been treated as out of scope for w3c discussions. I don't see why. It's part of the same web.

Yves: documenting how things work - and how things don't work. So people making regulation don't try to do things that don't work.

... Lola's example on accessiblity. I18n is another example of telling people how to do things so it works for many people they don't think about. Don't know if we should be more explicit. Definitely in the mission of w3c.

Sarven: one "so what" is the assumptions that are being taken.. a lot of the things we're trying to do are for the people who are currently on the web and not necessarily people who haven't made it to the web. Who is the commons for? People who are struggling on the web? Integrated with everything going on on and off the web? Or getting people more on the web because there's a net benefit for their lives - but we are assuming what will be better. We haven't tracked down what they really need. What are we trying to improve? Whose commons are we talking about?

Matthew: Very good examples of areas we do want to tell people what to do. In terms of building w3c's credibility within the very much wider standards area one way we could do that is by neutrally describing in a way that has consensus this is how it works right now. Once we've got that and people know we are trustworthy they we can put positions forward that says we shold be making it accessible, internationalisable, private, secure. THese things go in parallel. We do ahve relaitonship building to do with other areas. We don't necessarily know what things governments might be thinking of doing for all sorts of good reasons where we don't know what the ramifications are going to be becuase we dont' know they're even thinking about it. They might be trying to do somethign right but they don't understand how the technologyw orks so it goes horribly wrong. We want to avoid that sort of thing. That's where education and awareness can help. Both are needed.

Dan: "who is being harmed the most by the current web" - we can use this in prioritisation of our work. We need to incorporate that into our thinking.

Jeffrey: a couple of avenues of future work to keep in mind for the rest of the week.

* describing what's going on.
* making recommendations at architectural level possibly for governments making regulations
* drawing down on this to design principles level

Could be three documents, need to decide when and how to publish. Keep thinking and pull it together over the course of the week.

## Introductions

*Introductions for each person, including one non-web thing about them.*

## Needs for this week

*See also the photo of the flip chart - I tried to ensure these are a superset, but may be msising things.*

* Patience, love, respect (earned)

* Explain things clearly

* Questions

* Assume good intentions, supporting each other, be aware of your conversational style

* Be aware of cultural and language differences

* Curiosity

* Speak clearly and make usre people can hear you (inc. for cues, clarity)

* Delivery mindset

* Be aware of your own filters / bias - your mindset is tainted by the work that you're doing.

* Hold space for others' strengths and limitations

* Be aware of others' tech / backgrounds

* Leave room for humor

* THere are people with more/less technical backgrounds - people who don't come from coding etc. backgrounds shouldn't worry about their expertise - feel free to speak up. You're not an impostor - your own exprtise is valid.

* To help the scribe and people on the meet - please don't cross talk / hav eside conversations.

* "Yes, and" energy - instead of stop energy, think how you can build on a point. Helps make the conversation more collaboratie than combative.

* Consideration for economic diversity. Support IEs.

* Be mindful of the pressure you may give to others to do something. We could be delivery/action-oriented, signing up to things, but there's also the funding/time we have available to the group. Some may be able to put more time in than others. Not everyone's on the same level to produce.

* What do we need from eachother when conflicts arise? [More for chairs part of discussion.] Some shared responsibility as well as with chairs. People need to be intentional when blocking consensus (which everyone has the right to do - but do it when it matters). Pick your battles.

* Prioritise - be willing to say no. Be willing to ask for help when you need it (and provide it when it's asked, if you can).

* Socialisation outside of working hours. We get on, and it helps avoid conflicts.

* No shouting.

* Tell the chairs what they can do to improve.

## What do we need from our chairs over the next few days?

*See also the photo of the flip chart - I tried to ensure these are a superset, but may be msising things.*

* Q: Or after that?

* Get us to decisions. We all have lots of opinions and lots to say. Chairs should help us focus.

* Building on the different personalities - chairs can help with balancing out everyone. Facilitate participation. Structuring the discussion so that everyone is given a chance to speak. E.g. using rounds when appropriate.

* Limit tangents. Parking lot strategy.

* Ensure that everyone feels heard by the end of the conversation.

* Minimising groupthink and ensuring that dissenting views are heard and are part of the conversation.

* Taking collective ownership of all points.

* Encourage questions; identify and highlight misunderstandings.

* Learn to step aside. When your responsibilities as chair are something you should be setting aside - recognise when an issue is one that you care about, and step back as chair and make sure someone else is able to cover for you. Delegate.

* Ensure that a conflict/circular conversation isn't going on too long.

* Follow up with people to see how they are feeling after. Work together to try to find a resolution.

* Enforce break times.

* 60 mins is the upper bound for any session (keep to less than an hour and have a break).

* React to how the session is going with respect to management (move on, or find aa way to keep it going, even if after a break).


-----

## Societal Impacts

Sarven: presents https://csarven.ca/presentations/societal-impact-questionnaire-tag-f2f

... hope to figure out direction, and what we want, identify gaps, citations needed, make sure it's grounded on other research. Collaborating and aligning with existing groups, w3c and elsewhere. Produce guidence. Introduce it into the explainer. Right now it's a draft note. It will evolve.

Dan: we were telling people in the design review process things that were like asking them to consider unintended consequences. Started to talk about dystopia avoidance. Breaking the user contract of the web. Fits well on top of ethical and privacy principles.

Amy: it's a conversation starter, not a pass/fail or tickbox exercise. And making some of the ewp work 'actionable'. Also tension around the amount of work this takes.

Jeffrey: what are the next steps?

Lola: Even thought this isn't a checkbox exercise, think about how we can use the other existing documents, to reinforce the things we want people to think about in the societal impacts questionnaire?

Jeffrey: we have a lot of questions that people are expected to answer. How can we make that process easier for the feature proponents so they don't miss stuff.

Yves: should we take privacy and security questionnaire out of our template?

Tess: I'd keep it in

Marcos: chatgpt specs and research to make it easier to do the questionnaire

Dan: I haven't had a good experience doing that kind of in depth analysis.

Amy: We can think about how to make it easier, but we don't need to give specific answers.

Martin: seen a proliferation in checkbox chasing as not necessarily being constructive. THe questions are the ones we should be asking. WE don't frame design principles as a set of questions. "Does this apply? If so have you followed this advice?" We ask people to understand competing tensions and engineer. We could discuss whether this is the right form to be engaging.

Sarven: questionnaire is more for the spec authors to reflect on what they're doing and the groups that they're part of. Not so much for the TAG stamp of approval. If the use AI to get the answer that is not helping anyone even if the answer is good. We need to know how the group came to decisions. It's an educational point. PWE has taken initiative on improving meetings - we need to improve community's understanding that it does have consequences. They need to take time to digest what they're doing.

Dan: Disagree that this should be a set of principles rather than a questionnaire. However the point is different from the dseign principles. It's about getting developers to thinka bout it in terms of unintended consequences that might be out of their comfort zone. Not sure a questionnaire at the time of a design review is the right time. Can we reframe it in terms of training that we offer to people coming into the w3c community.

Lola: similar to Dan's. We should discuss how we can partner with other orgs, CGs, this is about change of culture in thinking about how people who are creating speces. Other orgs who can educate us and we can do developer outreach and spec author outreach and educate them.

Xiaocheng: Should we add real examples to the questionnaire?

Lola: also about co-editorship

## Enshittification

Martin: the idea of e14n (en13n?) - market capture and abuse ... create a service, created by injecting VC money ... therefore half the price of what it should actually be .. and then you have to exploit access to those people .. then leads to behaviours like anti-competitive actions, selling your users to other business, eg through advertising, predatory data practices.. If you're not at the table, you're on the menu.  Platform owners sell customers to other business - and then treat those businesses as their primary customers. Then they screw the businesses they come to depend on for revenue... I'm more concerned about this as "the web"... I want to discuss what we can do .. about the trends where individuals are exploited. We need to pin down where those leverage points are in the web ... inherent in its architecture that allows people to be exploited.  E.g hyperlinking is an essential nature of the web but also can give source and destination ability to exchange information about the user and therefore create profiles...  Architecture of the web could drive things to become worse...  Other things like performance - it's virtuous but it also can be exploited.  

Hadley: what would you like to do with the breakout?

Martin: explore the basics: how the architecture of the web can be used to exploit people and what we can do about it.

Lola: Would be good to look at how other bodies try to address this problem, if they do.

Dan: I would like to point out that e14n is a new term we can use.

Jeffrey: Think about what allows a company to get away with these practices.  Competition might be a factor.

Tristan: Doctorow's 4 phases: 1 ? 2 ?, 3 stop serving your own users; 4 you die

Mastodon doesn't enshittify, it didn't take VC money

https://en.wikipedia.org/wiki/Enshittification

Lola: most of the big financial input to the W3C is from companies that have these practices

Xiaocheng: exploitation .. a critical question is what sort of exploitation might be OK.  the web cannot exist without monetization, so is that acceptable?  How can sites profit from people?

Amy: Reminds me that there was an issue on EWP a while ago about economic models for the web, so it ties in with that work that way.

Dan: Yes and

I was going to talk about there is definitely a bad corporate tendency of bite the hand that feeds you.  I think that Google has been guilty of this in terms of bringing in some of the same factors.  Can we bring that concept into the discussion.  Brexit is a non-tech example of that sort of thing.  Might be related to the web as a commons work.

Hadley: What can we do?

Martin: short term - understand the problem better, without solutioneering just yet. Scope the problem we could solve.

### Breakout

Jeffrey: What can we do?

Peter: Burn it all down.

Matthew: What's the problem, and what in the architecture contributes to it?

Martin: Hyperlinking? In the technical architecture; and the economic architecture. Incentives are as they are.

Peter: It's wholistic. Have to attack it on all fronts.

Tess: During expectations setting, Marcos said something about when dealing with an area with people who have domain expertise. This is just Cory's name for capture and rent seeking.

Peter: Remedies from the past all involve things like guillotines.

Jeffrey: Maybe e14n is the wrong term, this is just about monopoly.  Competition law has worked.

Amy: Are there things that we can do with regulators?

Jeffrey: Yes and also try to break the monopolies using technical means

Peter: Nothing we can do to the web to solve the problem outright, but we can do more to make it harder.

Tess: (Poor imiyation of Robin)  The focus on Atprotocol on things like credible exit from the service.  Human identifiers are independent of your service provider, that sort of thing.  We don't any proof that atproto will pull of the win, but they are building this.

Jeffrey: they have identified the right problems, but I'm not convinced by the solutions they put forth

Peter: If you make a system that allows good actors to be good, without means to incentivize that for bad actors, you don't get there

Jeffrey: Sanctions can work.  Search algorithm changes pushed people to HTTPS.  We don't like that that power exists, but we might look for non-monopoly ways to achieve that.

Matthew: COntent authenticity tie in as well.  Societal education primarily, not tech.  Giving people a means to move away is essential.

Martin: .. but not sufficient

Matthew: Central authority to apply consensus-based sanctions.
Who might we engage with in order to find the missing pieces.

Jeffrey: monopolies are fought with antitrust, I don't know of other means

Martin: Not only monopoly problem. something egalitarian. Google is the best of the bad actors in this regard. GIves you control, is transparent. Doing the bad thing in the best possible way. Competing tensions in business imperatives. Incentivesd to keep it on the brink. If it slides down a hill they lose. Goes the other way they don't make as much money. The rest of that market fighting over the scraps, the good behaviour is out.

Jeffrey: the average site's behaviour around showing ads and stealing attention has enshittified. THat's not a monopoly problem. Those sites have no market power. NO downside of being a little bit worse than your  neighbour because users can't tell that you're going tobe. The search ranking algo should have incorporated that, there's an arguemtnt hat because google gets paid by thos eads it's not doing as much as it ought to

Martin: ecosystem as a whole has shifted gradually over time. 25 years ago you could put ads up and it was annoying. Advertising has got better in a sense but people were making money of relatively lower amounts of traffic. But now someone can have really decent viewership, high quality ads, and get no money. Which is objecively worse.

... Advertising is at the root of a lot of problems, but not the only thing to talk about

Peter: more of a vector. Enabling tech, not necessarily the driving force. Google has this incentive to maintain equilibrium.. but if it was perfectly maintained and everyone else was at that it's not good enough

Martin: concerned about the adjacent digital credentials stuff. Spent a week on vacation in Europe; you simply cannot do business with any number of new entities without also giving them your life story. I didn't have a functional phone number. It's terrible.

Jeffrey: we've been talking about authenticity, reputation, trust: https://docs.google.com/document/d/1wTFafdHa-o3OYCKmYzEJGROrpSoxXN6DNXPltzdiUzg/edit?tab=t.0

Martin: part of it is building trust in people you do business with

Jeffrey: part of it is. Sharing trust. In a way bad actors can't pollute it. If I had a browser extension told me that people like me like this site I'm about to go to, but if people like me thought it had too many ads I might not click

Peter: how does that system know that I"m like these other people without knowing more about me than I'm comfortable with

Jeffrey: recommendation systems should be easier than they are. YOu've rated things. YOu can be similar to people by matching their ratings

Martin: slippery slope is difficult. BUild a reputaiton system and someone attacks it.

Peter: useless because gamed

Jeffrey: none I know of try to do personalised ratings. Global.

Martin: it's difficult. Reputation of people visiting is tied in more than the reputation of sites. Sites ask for information to manage risk of doing business with bots and garbage - don't want to throw away resources. We could build systems to deal with unique cases.

Matthew: Something more specific than tag enocurages decentralised solutions?

Tess: privacy pass?

Martin: not the solution.. but in a class of solutions. Recognising that is an option and implementing that.

Peter: what can we do to fix linking. Not sure I entirely understand the problem. Referrer information?

Martin: if I follow a link the website that I leave will know that someone left, and have some concept of who that someone is (information you've given them or they've got from elsewhere). Site that you arrive at knows that their conception of you (which may be different) arrived at this time. Timing of those events and proximity is enough for those sites collaborating to link those two. You can do that at scale with high fidelity and nothing you can do to stop that. Navigation tracking impossible to block. It's a property of the web that we celebrate. It's an essential property.

Peter: offhand, flood it with misinformation. Prematurely prefetching all the links. High bandwidth costs

Tess: high level reputational costs to fire click handlers on all the links

Martin: websites won't like it easier, drives up costs

Jeffrey: does the ability to track.. same as enshittificiation

Martin: no, just a natraul property of the system that allows for the exploitation

Jeffrey: a particular kind of exploitation. Doesn't lead toa  worse user experience on those sites. Means that your data gets out and you have a worse experience in the world, but I don't think it centralises things or leads to sites being worse in other ways.

Martin: it's the wrong term to use your'e right

Jeffrey: it's a privacy problem, but don't know that it goes beyond that.

... escrow systems. if a site does something wrong. Seems like something we've been opposed to in the past. If this is a reason to say let's investigate that it could change priorities

Martin: yeah. It's goign to depend a great deal whether tha's the right recommendation to make

Peter: applicable when concern is fraud or other crime.  A lot of fingerprinting going on in the financial space in the servie theoretically of preventing credit card fraud. Using unsanctioned tracking as a how-to. Accept fraud is a big problem that needs to be addressed. Either abuse people or use an escrow system.

Jeffrey: not sure people are collecting data only for antifraud. Also selling your behaviour.

Martin: a bunch of rules about how credit card info can be handled. A number of websites collect credit card no, name, address, and necessary peices for payment. The payment service has an iframe that covers just the credit card. They're the ones who get the address and name information and pass it on to the payment service. They're not obligated to follow the same rules

Peter: the site I'm buying something from does not need to know my billing address when it's different from shipping address.

Matthew: partitioned pop-ins we were having the conversation... people odn't appreciate where the information is going. We'r epredicating a lot on the fact that people have been trained to trust certain areas of the UI. It's a big assumption. It was successful wrt to doing it the right way round with the transition to https. Is there anything we could suggest that would be a similar sort of indicator to show that your information is going to different places that users could look out for.

Tess: there was a browser extension that EFF did that was shwoing you information flows and this cool visualisation. Not production UI.

Matthew: TOS;dr was great.. is that a tool?

Jeffrey: tools that with some work you can figure out if the site you're on is good or bad or inbetween. But no way to quickly just not visit the site. COmes back to the reputation service. If you do the work to figure it out your friends should get the advantage of that

Tess: market dynamic... google has done that work because it's the secret sauce of search ranking. Google is not in the business of sharing the secret sauce. Not going to have an api for that. Incentives are directly in conflict with the desire for such a service.

Peter: our entire economy is built on a ponzi scheme. As long as people are playing that game they are on this track

Matthew: who do we partner with to put the message out

Peter: much bigger problem. What can we do architecturally to weaken the impact or provide alternatives to people who don't want to be on the treadmill, make it harder and more annoying, take some of the tools away. And point out the problem to society at large

Martin: Activitypub ecosystem... 5 years ago it was a joke. It had time to mature and be ready when the world shifted. Are there other things we can do that with?

Matthew: describing things as they work and as the could work can be useful. People who make decisions about things don't realise there's another wayt o do things. This whole thing about how much data are collected just to enter into a transaction. Don't like halls of shame but for example we could raise awareness in our day jobs. One example is there's a restaurant with the most amazing web app for ordering the food and doesn't take any personal data at all. Big up these examples of the web as it is today you can do these things. These are small businesses.

Peter: sustainability over time as people become more aware. We have to get rid of the notion that companies have to be perpetually growing. INcentivese small players to not play like the big players. Be different, better, serve as an example. GIve people the tools to monetise their sites without relying on advertising and selling users data.

Jeffrey: and if they do sell their users data theyc an charge less for their main product... WE have to give the users whose data might be sold who they prefer as they're browsing. Provide incentive to be good.

Peter: and the sites to provide sites without opting into the bad behaviours.

Jeffrey: they already can

Peter: going back to credit card fraud.. a while back I was building a site. Totally ethical, clean... then when you want to get to the credit card payment you have to drop a script in that learns everything about you. I said no way will I do that. They said it's optional. BUt everything up to that point implied you have to.

... when you push back on them they acknowledge they'll still take your business without screwing users. But how many push back?

Jeffrey: can we provide instructions for how to do it without the script? A clearing house.. if you've pushed back and succeded, put it here. Suspect that will prevent banks from ..

Tess: w3c would not want to be that clearing house

Peter: if a website just had to implement a few calls to the browser and the browser handles the ui and data gathering, website is out of the picture, browser could be making sure the api is behaving ethically provided the browser is incentivised to do that

Martin: web payments does most of that

Peter: we can have some impact by educating people that it doesn't have to be this way

Amy: the name of a finding: It Doesn't Have To Be This Way

Matthew: web monetisation have found a way to hook into financial networks in a way that is acceptable. Does anyone have experience with that? Does it solve a right problem? DO it the right way? Simply no other alternative

... Portability of data and handle is interesting. Can we make it a virtuous cycle and improve incentives. Sort of happening with fediverse. What can we do to help the market work better?

Tess: concentration of power and markets. The only real solutions that have worked in the past have been regulatory in nature. Take digital credentials work.. there have been a number of laws lately where adult websites are being required to gather information about the visitors from their government id. Several states in US have imposed this. There's no technical means for them to collect just the information they need. THe defacto implementation is send a photo of entire drivers license. Lawmakers could be better informed about data minimisation, more privacy preserving approaches. Say what you will about the use case but we could help them do better. Less instantly enshittifiable.

Jeffrey: I think oru digital credentials working group could produce guidelines

Peter: the laws are not written by the lawmakers, but by the lobbyists who want to capture this data.

Matthew: what can we learn from Estonia?

Martin: Sweden has bankID - it's a mess. Adhaar in India is a disaster from a privacy perspective.

Peter: we can provide the tech to do it right but if the incentives are to abuse the system they'll keep abusing the system

Jeffrey: can we make reporting of inappropraite use easy

Martin: good angle

Jeffrey: if the user notices the page is collecting ID when tehre's no need to

Martin: pinning my hope in provisions in eIDAS legislation. In the EU in order to get an EU national identity you need to be registered with the identiy provider in that country. You have to thave the things your'e going to use in a register somewhere. If you're accesing personal information you have to justify it to the government and there's a public record of that justification. IF we put it in the browser you're going to find that justification and show it. If you don't get that justification you don't get any data. Don't know if we'll be able top ull that off but that's what I want to see happen. Doens't fix the problem because there are business out there that find it easy to obtain the necessary credential an dhave justifications that are a subset of the actual things they use it for and abuse it in various ways. We do what we can.

Jeffrey: in the US if you make a claim about your privacy practies that is false that's a hook for the ftc to look into you

Martin: the concern is once you've got the information then you're into gdpr land. Has a number of reasons you can use to justify use of the information

Jeffrey: you don't have to be honest in collecting with the user..

Martin: there are ways to be honest without being honest. Seen from a number of different companies. They need this information for this purpose. Which is a true statement, but doesn't cover waht they do with it next. Then you can use legitimate interest.

Matthew: press can see it?

Jeffrey: and browser can show it

Tess: api just fails

Peter: disheartened by how many people just do it because it's the way it's done.

### Summary

* Much enshittification is about monopolies. We don't know examples of fighting monopolies without regulation, either utilities or anti-trust.
* A distinct kind of decreasing quality is websites showing a bit more ads because their neighbors are.
* It's driven by capitalism. Mitigation is all we can do.
* How can users know which service to use that's least-enshittified? Reputation?
* Privacy-preserving services.
* Identity escrow to fight fraud without enabling data sales.
* Look for tweaks that can turn markets into a virtuous cycle. Data portability?
* Hook into laws that require useful things. E.g. Digital IDs might show the use the data will be put to.
* Highlight examples of good sites that just provide a service without collecting too much data.

## The Web in China

[Slides](https://docs.google.com/presentation/d/1AwWg2h3gfhvytdTzM6P4nrKrkMtws_tmTXaj1v8mJVI/edit#slide=id.g33285fed7c8_0_0)

Xiaocheng: 1.1B internet users in China as of 2024. Over 99% of users use a mobile device. Non-conventional devices: TV, wearable. Just 34% of users use desktop. Only the desktop users use a browser; others don't. Recall that 10 years ago that "the Web is dead" because the ecosystem was taken over by apps. It did happen in China: taken over by apps. Everyone is usign web-like technology, especially MiniApps. 

Xiaocheng: MiniApps are like PWAs. It's the successful PWA: lightweight mobile apps. Flexible liek web, but native-like experience. What made it successful is that it's not standalonne, but rather built on a super-app like WeChat. Very closed and centralized ecosystem. That made it successful. PWA wants to avoid this, but it also gives traffic.

Martin: What do you mean by traffic? Visits?

Xiaocheng: Yes. Pretty closed ecosystem. We have a miniapps WG at the W3C, but tencent is not a participant because they're so successful. Technically, there's architectural evolution. It started as a hybrid app with a webview. Evolved into a 2-thread architecture, which led to better performance and better isolation. [Shows what a miniapp is like]

Xiaocheng: The user system is integrated with WeChat. You still have to log into the miniapp, but it prompts with the phone numbers registered with WeChat. Payment is WeChat Pay. 

Martin: What's WeChat's cut?

Xiaocheng: I don't know.

Sarven: Is WeChat among other superapps, or a silo?

Xiaocheng: There are other superapps. AliPay is one - can open DiDi..

Sarven: is starbucks also there? Does a service expose themselves to all of these different superapps, or one code works on all?

Xiaocheng: starbucks is also here, it's similar. From my experience miniapp authors are trying to reuse implementation as much as possible but do need to write adaptation to each platform. There are adaptation solution providers

Hadley: is the goal of the miniapps wg that a developer can write it once and use in multiple places?

Xiaocheng: I don't know. Their last spec is about the package format. 

... typical architecture. 3 parties - miniapp authors - html and css and js (they don't run in the same process - html/css in webview. JS runtime separate). WEbView as UI rendering tool.

... the miniapp platform provides framework and native app.

... network and navigation tightly controlled. App part intercepts all network and navigation requests from the author code.

... Lower layers - the browser in the traditional sense. AppService is a JS runtime like Node, then the native OS.

Dan: you mentioned people don't use web browser on their mobile phone. How far that extends? Do phones not have a browser? What if you need to find the opening time of a national park or something? Some inforamation that might not be available through a miniapp.

Xiaocheng: in that case I'd use a map app.

... Also you can search. I was told the newer generations of Chinese don't use a search engine at all. Likewise you see QR code pretty often. Payment, or to open the app of a shop or some restaurants. When you see a QR code our experience is open camera, scan code, get a link and open the browser with it. In China the experience is after seeing QR code I open a superapp, typically wechat. Then scan. So you need to know which platform's QR code it is - is it a wechat QR code, is it an AliPay QR code. Good thing about it is they are compatible QR codes that can be used by multiple superapps.

Dan: it's one thing with STarbucks with a developer team. An independantly run restaurant with an app in wechat.. how would they do that? Would they have to negotiate with Tencent in order to get their app into the catalogue?

Xioacheng: afict registering a new miniapp isn't a very difficult thing. A small restaurant has a lot of solutions, you can purchase. Similar to uploading to Play Store.

Jeffrey: if we think of the superapp as a browser or UA, how are they thinking about the ethical principles and the user agent principles that we expect traditional browsers to follow. How do they protect users from tracking for example?

Xiaocheng: from my experience they do try to follow some but I don't think they are following exactly the same ethical web principles. There are also permission systems. Demo: privacy agreement and location request.

Hadley: the super app has your location anyway?

Xiaocheng: would like to collect more questions. What would you like to know about how these things work for users, companies, government?

Peter: why this whole system came about in the first place? Is it a side effect of Great Firewall? Is it because the web isn't usable?

Jeffrey: facebook has an in-app browser that tries to keep people inside it

Peter: are there political as well as economic aspects?

Xiaocheng: don't think the Great Firewall is a major driving factor. Can talk about in the breakout how these things evolved.

Lola: the miniapps WG has three working drafts. THe breakout can talk about what does the TAG need to learn and understand in order to review these. It seems like the web in china has a completely different working model than we're familiar with. What do we need to understand so we're not looking at this with a western gaze and say you have to do things in our way. But also keeping users in mind.

## Breakout on web in china

Present: Xiaocheng, Hadley, Marcos

Scribe: Hadley

Lola’s question

Web in china is highly centralised. And regulated. 

Why difference? Looking for an easy answer, blame on difference we are mostly familiar with. On Dan’s example, it’s the government. 

More complicated than that. The gov is playing a critical role, but the companies are shaping the ecosystem. 

So: what led to this ecosystem? Not because of the firewal. Before miniapss, WeChat and the like had a large user base. Built a more closed ecosystem on top of that. 

Minis started in 2016. PWA were young too. Web view with basic functionalities. Became successful, people started to follow this model. 

Role of the government: sometimes over exaggerated esp in western media. 

Relevant to our ethical web principles. 

M: what to deliver?

Suggest everyone get up to speed

X: someone else suggested this session. 
Introduce web in china and see what we can do 

M: fine. There are presuppositions on. Or understanding the dynamics. Came through in the questions we asked, like were minis motivated by the great firewall. 

You said we don’t see simolar examples outside echinan. 

I’d challenge. Ex: Facebook, which has opening times for restaurant, park. 

Those things are interesting. Cause risk: if Facebook is down, info is no longer avail. It’s on Facebook to decide if the content can live on or not. 

Parallel to the super app
Instagram. TikTok. Facebook. 

I search instagram for cool things to do in my city. 

Moves into the whole e14n topic too. 

Challenge what PWAs are vs miniapps. How we build PWAs, from the addition of a manifest, they were always built on the web architecture. Measure of success isn’t users adoption, it’s that all apps on the web are PWAs. Any page you can add to Home Screen. Users don’t always, but they are all PWA. That’s a shift. I don’t need to add a manifest, but I could. Do user has control over. When added to Home Screen, it becomes a PWA. 

Miniapps went down the route of needing a zip file and different permission model, etc. ceased to be part of the web in that sense. 

?: what happens to the same origin model?
They’re running a URI scheme, what is it? Not answered in the spec. 
Does it mint a UID for each app when you install it? Can it be used for tracking? 

What degree can a user control this?

App stores all work on the same principle. On tech and web standards, there is a point of departure. 

X: what does the progressive in PWA refer to? If I add it to Home Screen, it progressively becomes an app?

M: yes, as far as it integrates with the OS. You hand the running to the OS. Geolocation is integrated to the system’s geolocation. 
Notification Centre on macOS, you can toggle the parameters there, 

Will new standards make miniapps work better?

Marcos: no, if we need a new standard we fail somewhere. We may end up with new standards, but we want to resist that as much as possible, fix what we already have. S othequestion is: what is it in the current web architecture that did not lend itself to solving the problems that miniapps had? Is it too late now? Because these things exist in the world, what can we do at this point?


In china these things are already used everywhere, which is fantastic -- but they do have a point of deparrture. What does that mean to have these two competing platforms?

In the West, we could say we believe we have the same origin model, the permission model, this works. But then the superapps say we don't eneed www.whatever.com, it's all coming out of the same superapp.

Xiaocheng: I think of it as a debate between whether we should adopt it, or try to converge it. 

Marcos: they are not in conflict

Xiaocheng: leads to the question: do we want to add something new to allow the adoption, converge it or reject it?
I'm inclined to adoption. It's a huge ecosystem that is relying on the web stack. 

Marcos: but it's small compared to the number of websites 

Xiaocheng: over a billion users. The number of miniapp users is 20% of the total number of web users in the world.

If you want to say we as the w3c want to serve all the web users, then I don't think we should exclude miniapp users.

Marcos: right

Hadley: What should we do? What can we get TAG consensus on?

Marcos: is it too late to change the miniapps ecosystem? We built the web since 1993 or whatever, then miniapps came along... Can we look at what is great about miniapps that makes them so successful? How to fold them into the web? Where there was a point of departure from the web, like permissions, why was that done and can we find a way of converging?

Hadley: who is going to do this work?

Marcos: sounds like a big piece

Xiaocheng: I am involved in that work, at Atomic services making miniapps more like PWAs. 

Marcos: we could write a comparison, and why is each decision was made

hadley: what would help you in your efforts to make miniapps more like pwas?

Xiaocheng: I could do a comprehensive comparison, but I'm more familiar with performance. I want to maek the mini app archtecutre closer to PWA. They want to merge the two processes in the architecture, they want to merge the two threads. It's slow, especially the start up performance. 

I spoke to some IWA engieers at google, asked about PWA startup performance, and they said it's not a concern.

Marcos: I know it's a huge concern. Was also at Firefox OS. Even in iOS, performance is a big issue as well. 

Hadley: makes sense, that's where the majority of the processing would happen.

Xiaocheng: we found a big slowdown when switching from the miniapp architecture to a more PWA-like architecture. This might be wehre we can extend web standards to help miniapps.

Marcos: potentially. This sounds very engine-specific, but I'd be happy to hear proposals. That would benefit all web pages. 

xiaocheng: the main idea is to change the concept of what is hte main resource in a web app. irght now, its the html file, and everhthign else has sto be discovered from it. In the miniapp, it's the javascript, what all the business logic is implemented. I'm wondering if you can change JS or allow an alternative mode where JS is the main resource, so the startup order is: manifest -> javascript launched and then from this worker thread, we can open pages. So then the start up is closer to the miniapp architecture.

Marcos: that's interesting. It would need to be demonstrated: hey, I'm going to spin up this worker thread and it's going to dictate which things to ope. It's like a serviceworker style architecture.

Then,: what can that thing do? How do you keep it fast, and what privileges does it have? You suggest opening a view where HTML page can be loaded and displayed. 

What makes that faster than loading a web document/page/html file? You'll need the rendering resources at some point, but you think this will make it more performant?

Xiaocheng: in miniapps, we want JS to be executed first. To set up something, like initialization data, and then we're ready to render a web page.

Marcos: from the internet or disk? Maybe it doesn't matter

Xioacheng: locally or from the host app.

hadley: is a superapp a user agent?

xiaocheng: it does fit. It's managing permissions and it's hosting web content. and handling user interacxtions, and privacy, security. When we're designing superapps, a lot of considerations are similar to designing user agents. 

hadley: are superapps UAs? Does average user in china expect the superapp to protect them from bad miniapps?

xiaocheng: yes

marcos: what about the UA or superapp reporting your activity to a third party? Is there private mode in wechat?

xiaocheng: I don't think so.

Marcos: ok, so what does it mean for my activity to be reported. 

is it a user agent or is it a societal agent?

Hadley: so we could add superapps into the user agent finding. A concrete way of bringing this discussion into the rest of our work.

Marcos: Putting together what the differences are and why there are differences would be a huge hhelp. You've identified somthing that is not covered by webmanifest (having a route to launch a js file). Loading an HMTL file is slower than loading a worker context... it would help to see this is true on all engines. OR, helpful to see the benefit if we do it differently.

Xiaocheng: 

## Breakout on Societal Impacts

Present: Yves, Tristan, Lola, Sarven, Dan
Scribe: Lola

Yves:  All the choices we make have an impact on society... What is currently on the web platform that has a bad impact can be replaced? Socital impact is in collaboration with tech standards as tech standards have a societal impact.

Dan: Let's estabilsh the document, note, questionaire, etc

Yves: If questionaire it should be a note. Statement does not allow for evolution.

Sarven: We're leaning on the idea that we should double check with group for editorship

Dan: Yes, every doc we write needs an editor however, in reality the material comes from everybody and sometimes other people besides the editors merge PRs (although editors are responsible for PRs).

Sarven: The key is editors are first and foremost and authors are everybody, I'd like to +1 
Lola as editor

Dan: is everyone ok with that?

Group: yes

Sarven: Lola needs to update PR to add their name. Amy would like to be former-editor but continue as an author

Dan: There's no designation such as "author" but "contributor" may make sense, we should check with Amy.

Sarven: (tangent) Discussion about different roles, author and editor but contributor isn't defined.

Dan: That's how we've done it in TAG  

Yves: TAG uses contributors to identify people who have made significant contributions. "Authors" doesn't exist in TAG.

Sarven: Just to confirm, Sarven and Tristan current editors and Lola to be added.

Dan: I can do that now. Ok so that's that, Jeffery left a comment on the PR to changes the link to ethical web principles to a spec ref. I can approve these changes... A lot of what we discussed is related to the process for spec authors, we don't want to increase burden for spec authors. What other ways can we encourage people to think about these questions?

Sarven: It's better to catch people when they're starting to work on an idea as opposed to the back end of the process. The earlier the better, there needs to be a wider effort in training spec authors in being spec authors.  Amy mentioned that as well..

Lola: adding : spec authors are not created in the w3c. Usually these conversatons start in someone's host company... then they bring it to the w3c.  So some of these issues may already be decided. Especially for things like privacy standards... I agree there is a possibility for some training to happen at w3c but that might not fix it.

Dan: If the W3C training can be promoted into host orgs as a benefit, we may be able to bring these things even earlier in the process. 

Yves: W3C has training but more geared towards public and AC reps. But this can be a good thing, another way to make memebers understand the value they can get out of learning what's going on.

Dan: Dispute resolution training by Jory Burson is a good example, we make it interactive so it's not just somebody watching a video.

Lola: TPAC might be a good space for such a training.

Dan: I still think that such a training program would stem from this document. How do we get 

Lola: Questionnaire can be integrated in other documents, e.g., EWP, can say consider these questions in SI. It is to encouarge thought. "Consider who is at risk when doing this.." as part of a spesific EWP

Dan: What don't we like about current doc? Nobody seems to be arguing with content? Questions generated by Amy and others in TAG

Sarven: I agree. Either we get spec authors to review and see if it covers their own concerns, I'm not sure doc is reflective of what others have been researching. We should close gap for concerns others have e.g. Sustainable Web CG. I'd like to hear more.

Yves: Some questions have examples while others don't, would it be better to have examples for all questions?

Sarven: Issue 2 is an extension of Yves question. Things that people can relate to or understand... speaking of which, there's a PR that's to do with an example. It can be merged but folks can have a look - Lola to review. The PR (#14) addresses how to measure the impact of the thing that you're doing. 

Dan: I'm worried that the example is a bit complicated for the user/spec author, addressing a number of things. Good points but we're trying to put people in the right mindset to engage in the rest of the document.

Sarven: The example plays off the paragraph before - be mindful of what should be quantified/qualified.

Dan: It's valid but I'm worried about readibility as we're forcing people to engage with too many things in this paragraph.

Sarven: I felt that the main message wasn't as well captured as it could be hence I elaborated.

Dan: I guess it's pretty coherent

Sarven: I assume PRs like this, other people should be encouraged to give it a go before merge.

Dan: We can set up rule to mandate a number of people to review PR before merge. We shouldn't do this in GitHub as we don't want to create a bottle neck.

Lola: we want developers to engage with this document... I think tirhg tnow it's too verbose. I disagree with Dan - I think the example fits in. But I think the document itself needs a re-working. In terms of hte PR (14) I'm happy with it but ...

Sarven: Agree.

Dan: Let's merge the PR but Lola's point should be raised as an issue; simiplification of the language. We should be getting feedback and working independently working to simplify the language. We shouldn't get tied up in knots about rethinking the whole doc from the begining, we've had good feedback about current structure.

Sarven: this PR was a result of me trying to understand the doc but I think Lola's point is very valid. Other reviewers may have more to contribute so document will get longer.

Dan: Should I create tracking issue on issue?

Sarven: I don't know if this list from the [Collaboration and Alignment](https://csarven.ca/presentations/societal-impact-questionnaire-tag-f2f#coordination) slide is enough but probably a start:

>    e.g., Sustainable Web IG, Web Machine Learning WG,
>    Positive Work Environment CG
>    Accessibility Guidelines WG, Privacy WG, Web Platform Incubator CG,
>    Credible Web CG, Credentials CG,
>    Social Web CG, Solid CG, Linked Web Storage WG,
>    Data Privacy Vocabularies and Controls CG
>    ... (and that's only within W3C, ...)

Lola: a lot of this list is .. groups in w3c who are doing some kind of work where there is a societal impact.  We want to reach out to the wider developer community who are not in the w3c.  Through something like MDN for instance... Where they may also be using it as part of their work to do good thing.  E.g. companies that focus on sustainability. How far do we want to cast the net?

Dan: It would be useful to cast the net wider, but should be focused on people that writing specs or thinking about spec wiriting. Getting more people that are outside of the trad W3C working group would be good, maybe reach out to different browsers. Rick Byers has fedback and been supportive of this doc, we should ask him to get ppl in his org who are spec writers feedback on SI to improve it... Do we have a plan for getting this feedback?

Sarven: We'll probably learn alot even if we reach out incrementally. Going too far out may signal that it's finished rather than a work in progress. We want to make sure we get the kind of feedback we want.

Dan: in the early stage of EWP we reached out to tech ethicist to double check we're on the right path. Are there people like that, that we could we reach out to?

Sarven: I'd like to reach out to Positive Work Environment CG as they had presentations and training on [Running Better Meetings](https://github.com/w3c/PWETF/tree/main/RunningBetterMeetings) because they were also trying to figure out how to make that accessible to groups.

Dan: Oh I see, they're trying to get to the same audience that we have.

Sarven: Yes.

Dan: To Lola's earlier point, the people in these groups are already aware of societal impact. I'm more interested in getting into the minds of the people who aren't necessairly in these groups but developing technology with societal impact, those are the people who I think need this most.

Lola: ??? Changing people's minds and that's a difficult thing to do. Out of scope of TAG but ??? 
we need to reach these people... how to get into their minds... but on a structural and systemic level there is no incentive to care. We don't need to create such an incentive but we need to acknolwledge it...

Dan: One of the incentives that we can come up with is that consideration of SI can increase chance of positive tag review. 

Sarven: Even if we can reach to one person among the people that don't care, that can have some impact.

## Readouts

### E14n

Martin: we talked about numerous things... Summary above.  One of the key discussion points was talking about monopolies and the effect that they have.  One of the major problems. We did tentatively point out that regulatory action has been the only remedy that we're aware of. That's not in the TAG's purvue.  One less in that area : web sites don't have a strong incentive to be better than their peers in terms of ad load or other negative practices.. So we don't see the competitive nature of the web rectifying ... bad experience?  That's a pure capitalism thing. We can look for means of mitigation.  Reputational systems as it relates to services.  How do people know that services are going to act in a better way than their peers... Building up ways to amplify the reputational effects of good behaviour. From the other side: one of the reasons web sites collect personal information is to manage risk... that's one reason web sites ask people to offer a "stake". maybe we need to find technical mechanisms to deal with things like this. E.g. identify escrow.  If info is in escrow then it wouldn't be handed over unless there was bad behaviour. Also: turning perverse markets around. Data portability could be one thing that could help. If you can go elsewhere then it creates lower barriers to change. Mastodon / fediverse as an example. 

Dan: and the fediverse is designed so that you can change from one node to another

Matthew: we talked about the fact that lots of web sites collect lots of data about people... some of that may be down to people thinking 'that's how it works' and some services don't ask for data. we could highlight those examples... awareness raising. 

Dan: e.g. "don't collect gender [or whatever] if you don't need it"... https://design-system.service.gov.uk/patterns/gender-or-sex/

Martin: e.g. a web payment API that says "put this tracking thing in your page in order to use our service". ... presented as a must have requirement but not actually must have.

Jeffrey: we could be a clearing house... this person pushed back enough to resist the creepy tracking script. but that could conflict with w3c's membership model...

Martin: privacy-preserving technologies... my experience is that most of them exist to protect commercial...

Dan: I tthink of privacy perserving technologies e.g. Privacy Badger.

Martin: ad industry thinks of this like attribution info sharing.. the privacy preserving tech is to enable info sharing with scrubbing... that exists to that company A and company B don't send info to each other but still get benefits to the insights. 

Martin: we've identified a couple of areas where we could start poking.

[no consensus to get a document]

### Web in China

Xiaocheng: Diff & similarities between mini-apps and PWA. 

1. Help the convergence of mini-apps and PWAs? Yes, because they're similar. On exactly how, we don't have consensus.  Actionable: to study the differences, for example in permission system, security model. Miniapps are often local files, while PWAs use the origin. What led to these differences? How can we help miniapp users from W3C's perspective?

2. Super-apps: Compared super-apps and "user agents". Are super-apps user agents? Yes, because considerations are the same. Permissions, security, privacy. Enshittification because they have all your data. Good to include super-apps in the UA finding.

Hadley: Performance, but no conclusion.

Xiaocheng: Specific idea to make mini-apps more PWA-like by overcoming performance issues in miniapps.

Marcos: In a way that could benefit webapps as well.

Xiaocheng: 1 architectural difference is the 2-thread model. JS in mini-apps runs in a separate process. Some prior attempts to get rid of this, and run everything inside the WebView but on a separate thread. Performance ends up bad. Start-up especially: when launching a mini-app, want to start running JS as early as possible, but in current web model, HTML is the main resource, and everything else is discovered from HTML. Prior attempts have tried to start a Worker thread as early as possible to start JS early, but that doesn't work well. Change the main resource? Start a Worker thread with JS before loading any HTML. Discussion on whether we want that kind of model, and what privileges this thread should have. No consensus; it's just an interesting idea.

Martin: Model you described made me think of Workers too. Idea of running a Worker before loading the page is really interesting. In Miniapps, is that worker persistent across page loads?

Xiaocheng: No.

Martin: If I navigate the view, does it reload the whole thing?

Xiaocheng: If I stay within the same app, the JS stays around. If you switch apps, it's gone.

Martin: So we could do the same thing on the Web.

jeffrey: if that speeds up miniapps, it may speed up web apps too? Especially things written as react, they would benefit from running js first and having that create the HTML.

Jeffrey: Any new work items?

Xiaocheng: Do a comprehensive study of differences between miniapps and PWA.

Jeffrey: Can we delegate that, or do we need to do it?

Hadley: We could delegate unless Xiaocheng wants to do it.

Jeffrey: One way is to send some TAG people to participate in a WG, to ensure they actually work on it.

Hadley: Because we don't need to have the TAG name on it. Just want to know the information.

Dan: If the TAG's driving it, could be a Task Force. Also, what are some lessons from Miniapps that could be brought to PWAs.

Hadley: Hesitant to spin up a Task Force because this is just a piece of research. Unless they're also going to take some actions. I mentioned "the TAG name" because for some things, the value in what we write is "the TAG said", but in this case we probably don't need that.

### Societal Impacts

Sarven: Discussed the status. Agreed that Note track made sense. Statement may not allow as much room for it to evolve. Current/former editors, everyone else contributors... Lola, Sarven & Tristan are editors, Amy as former editor. We will acknowledge significant contributors... We'd like to catch people earlier in the process. But some conversations / related to authorship happen earlier on (e.g., at someone's host company), not necessailiry something we can target but good to be aware... We discussed training within W3C... Integrating some aspects of the questions into other documents, EWP or other principles, "Consider who is at risk when doing this.." as part of a specific principle.... We found adding examples to all questions would be very useful.... We don't want to rethink the document but we do want to make sure it is more approachable, perhaps less prose... We want to reach out to some of the existing W3C groups for starter feedback and we could reach out to other groups outside the W3C but that might need more time... Positive Work Environment had similar process for running better meetings, we can learn from them.

Martin: I've stopped consuming Privacy & Security questionaire because it's verbose

Marcos: Challenging assumptions is a better way

Lola: To clarify, when we talk about including these questions as part of other works, we mean as an example and reminder. We've SI questions for people to tihnk deeper what they're doing.

Dan: I agree with Lola. The primary use of this doc is not to have people fill out the questionaire as part of design review.

Jeffery: Would a societal consideration section in spec be useful? A way for spec authors to show how they think through these things.

Dan: W3C working on a human rights considerations, we should be working with them.

Amy: This may be an opportunity to support that effort

Jeffery: Human rights are individual, societal is collective, a word to combine both?

Dan: Human rights support healthy society

Martin: Consideration sections have started to proliforate. All important but documents with many sections which are boilerplate. 

Tess: This work should be inline, part of the tech, rather than an add-on.

Martin: Doing the work is thinking about all of these things. These docs should support so that they can do the work better.

Tess: Point of privacy questionaire is to think about privacy in the first place. My hope is that they can reflect this work in the design rather than just answer the questions.

Matthew: This is really interesting. I agree however, I find it helpful to have consideration sections and part of horizontal review and because sometimes it highlights how it has a bearing on the end user. E.g. [Compute Pressure API Accessibility Considerations seection](https://www.w3.org/TR/compute-pressure/#accessibility-considerations) explains to developers how they can use the API to make their app more accessible. Different audiences gain different benefits from the document (implementers, developers, mainly). Should we be making them more flexible?

Sarven: Most of the time we're talking about specs. This doc will be useful for people creating use case documents too as use cases highlight the issues SI hopes to address.

Dan: We don't have a way to engage with people while they're coming up with use cases.

Jeffery: The explainer explainer identifies what to do when creating a proposal, maybe this belongs in there.

Dan: & explainer explainer is becoming a note.

Tess: I think sometimes people think that because a use case has been idetified it must be addressed. not all identified use cases should be addressed.

Dan: We have a doc that mentions not launching a feature as a viable option.

## Sustainability

Scribe: Sarven

Tristan: Sustainability can be very different things for many people about energy. Projection of energy consumption for IT is increasing - a lot coming due to AI. Another issue is climate change. The CO2 evolution shows many instances where we should've stopped/increasing/reduced. In no climate policies goes up to 4.1-4.8C temp increase. Current policies shows 2.5-3C projection. Still not good. Where we should be is on 1.5C pathway. This is one of the most important things humanity has to take care.

Tristan: Climate change is extreme weather events that become more frequent and powerful at various places on Earth. A lot of people are concerned but not enough people are concerned overall.

Tristan: I'd like to discuss plantary boundaries (climate change, biodiversity, land-system change, fresewater, biogeochemical flows, ocean acidification, atmospheric aerosol loading, strastospheric ozone depletion, novel entities.) Who is familiar? Started in 2009. There were 7 boundries and 3 were crossed. More than what the planet can provide. In 2015, 4 were crossed. In 2023, 9 assessed and 6 are crossed.

Tristan: For biodiversity collapse, the issue is we are killing animals pretty much everywhere. These biodiversity offering important services, e.g., clean air and water, making soil productive. If we kill life around us, we are killing ourselves.

Tristan: Climate change is important but it is one of the 9 boundaries. If we narrow the boundary, we may fix it there but lose elsewhere.

Tristan: How can TAG play a role in this important topic? There is a Sustainable Web IG. I'd like to spend more time with them to understand the work that's being done. Maybe we can leverage their work. Another question is how we else we can focus on the other boundaries. What can we do with TAG to make it work?

Dan: Thanks for setting the stage. One thing comes to mind is Web is set up for scientists to share information. And scientists sharing better to solving these problems. Is there we can do better for scientists?

Hadley: Data standards and schema work used to be done at W3C. A lot of it has moved away in the past ten years

Jeffrey: What kinds of inmpact do computer systems have outside of energy and climate?

Amy: Disinformation?

Martin: We are contributing a lot.

Tristan: We do not see or not interested in the mining of minerals for example. We see tihngs being used in certain countries, and we have stuff end up at our desks. That's far away from us. We don't see the mines and the waste and all of that. ANother thing that we don't see is data centres. We know they are there but not like we visited them. They are invisible to us.

Lola: Something that would be good for the group to explore; the lifecycle, from networking side of things to what the users see. And impact on these planetary boundaries. What questions do those bring up to ???

Tristan: re data centres, last time I chcked, they impact 5/9 boundaries. Concrete is terrible for CO2, destrying life. Again, a lot of this is invisible to us. People see "the cloud" only.

Matthew: If there is performance, wondering there is resilience as well. Can TAG say anything about that given the overview? Another question: heard there are initiatives that are able to use tech to verify the supply chain of things, fair trade or safe/responsible minening. A lot also on blockchain, and wondering if non-blockhain or digital credentails stuff could help .

Yves: Blockchain is not always global / decentralised or distributed. There are local.

Amy: Existential dread in the room sinking in the room is great. Spending a lot of my time on this stuff nowadays. Nice to see it watch it land on others. Let's not bring too much of the stop energy, and there are stuff bigger than the web. This is a global problem. So many facets. How do we focus back down to architectural issue? Otherwise it is too much and won't do too much and get into circular arguments about mining bitcoin with renewable energy. In my local community, there are council initiatives on sustainability and what to do on local gov level. Which again can feel a lot like moving the deck chairs on the titanic. Everyone needs to move at once to be effective. but a parallel track of that is too late but then we are looking resiliance planning. what can the web do to make the lives of people on ground better when things are going wrong (power outages, local community coordination). and plan for the post-apocalpytic web (but maybe not pitch it as extreme to that).

Matthew: re carbon.txt

Jeffrey: IG hasn't started yet and we should push them to talk.

Yves: When we present sustainability to other people as a scary thing but if we tell them that small changes can happen positively and bring more performance... the positive of getting more performance for websites may be better for people... ???

Martin: there is the "the slow web" notion. in a lot of cases, the content you're delivered may differ. there are all sorts of security applications. and getting the same has benefits. if same content, can distribute and more resilient. If you don't personalise every page.

Sarven: [academics using web standards to share scholarly articles and annotations](https://csarven.ca/linked-research-decentralised-web), open reviews, where data is stored and granting access. It narrows down some specific problems. There are major third party publishers (eg Elsevier) that charge 1000s of $ to put a single pdf on the web. You can publish unlimited 'papers' with your own hosting and storage and web standards, archive-friendly and accessible... for $100/year. As far as economics it doesn't compare with what we have available. It's a social problem rather than a technical problem. Requires systematic change.

Matthew: re reputation systems, the two way you need. one what sarven was saying, mechanically you can deal with this stuff but only deal is with peer-review, in a decentralised, .. is this a common architectural thing? different parties going to different places. common thing that's going ot be needed. people can make up their own mind about instead of being told.


### Breakout

Present: Tristan, Jeffrey, Sarven, Amy

Amy: How can we redirect the IG to look at systemic effects? Their current focus (last I checked) was on individual website carbon footprint type stuff. Thats' a great way of engaging developers, but frustrating when it's the only thing they're looking at.

Tristan: They have a lot of energy, but we could nudge them into a better direction.

Jeffrey: should our goal be to write some guidance for them?

Sarven: I will probably join that group. Not sure if we - at least I - are in a position just yet to provide guidance w/o completely understanding what they're up to or considering.

Jeffrey: they're stretched quite thin. Sustainability on corporate responsibility as well as planetary sustainability. UX design is the first section of their document. They don't quantify things.

Amy: Hard to quantify anything, even experts find it difficult. We do need to get better. It doesn't matter what the numbers are lets just try to improve the situation.

Tristan: We already have many cases some numbers.

Jeffrey: 

Amy: Perhaps an analysis we can do on their documents, and they can look into focusing on TFs. An overview of how sustainability intersects with a lot of existing work, and then a gaps analysis, might be useful.

...

Jeffrey: There are lot of detail for each consideration in their document. Seems like they've put a lot of thought and research into it. 

Tristan: 

Amy: Backward compatibility. Washing machines last 30 years.. why not the phones?

Sarven: carbon.txt issue .. I've asked sustainable web IG whether they have a way of letting consumers [discover data and reports](https://github.com/w3c/sustainableweb-wsg/issues/22). They didn't, even though their document talks about the things you should be making available. I created an issue about that. It says things must be machine readable, but doesn't say how. Help the data become more easily accessible from these websites. That will help us get the real data to run analysis. All the things they want to do is doable through the guidance they want to provide. All sorts of schema and data initiatives at W3C that help to make the data discoverable and reusable. There is evidence people want to implement it like in carbontxt but they were doing their own thing with well-known and plain text. Needs coordinated effort. I'd like to at least encourage that low-hanging fruit further in the group.

Jeffrey: anything built end to end makes it easier to do the next thing. Good direction. carbon.txt doesn't let a user say my visit here cost xx resources. Getting that through end to end so eg. Google Cloud can say use of thsi particular service costs this much energy or water or whatever per request and websites can say I called these things so it cost this much. Some way to connect all the way through.

Sarven: search results ranking could account for this

Jeffrey: browser extensions could mark results even if ranking isn't effective. GOogle has done ranking by website goodness. There's precedent.

Amy: complexity. Two things. There's sustainablity _of_ the web, which is purvue of sustainable web ig, and maybe we can provide guidance there. But also sustainability efforts in society _using_ the Web. How can the web can be used to help coordinate better? From disaster relief to scientific collaboration. What positive message to use the web for good for sustainability. And then if anything, are there architectural changes that would help.

Tristan: local copies of wikipedia for example. open street map making coverage of Haiti following major events available offline. google maps was not doing.

Jeffrey: sharing peer to peer when internet is down using local web stuff.

Sarven: lot of thoughts around the scholarly communication. Not well versed on what to do to have an impact on environmental impact. Superficially, academics publishing through major publishers is costing a lot of $

Jeffrey: and reduces access to that research

Sarven: costing money that could go into libraries or education systems. That money could be allocated for other things. Besides that I'm not sure how saying using web standards is going to help reduce our footprint or energy use.

Jeffrey: not sure anything for the TAG to do in improving scholarly publishing. It's already possible. There are social pressures.

Amy: Sarven has been hammering the web conferences to publish using the web / standards for years and it is unbelievable how much resistence there is. THe common thread here is citations, chain of trust, credibility work. All the pieces exists. Web Annotations have skirted the edge of this. BUt nothing has caught on. Scholarly publishing is a possible concrete route to proof of concept this.

Sarven: it's a social issue. Publishing in a journal makes something 'scientific'. But they're conflating the notion of credibility - certification and registration. Putting something on the web doesn't mean something is credible or trustable. You've registered it, it can be referenced. The certification is a separate dimension, where there is a peer review system that says that thing has value. Academic systems forcing academics to waive copyright or use these journals to put something out there - or it doesn't count. THe system does not acknowledge your work.

Jeffrey: Can we use some of the peer review systems to do some of the credibility work? There are non scientific things that could be more trustworthy if trustworthy people endorse this. COuld we pick up some of those systems?

Sarven: there's a bridge with the authentic/credible web initiative. Underneath they're all touching similar systems. Domain expertise is really important, but you still need to know who approved it or what they approved (some of the arguments in a document are approved and some are )

Amy: There are different audience. Doesn' thav eto design one size fits all. There are people that want a highlevel and other more specific. All kinds of angles and different tools for UCs. This is one part of the problem that is huge. When you zoom out there are of other things of equivalent size.

Jeffrey: Also like I can put whatever I want in a carbon and important to have community to verify.

Amy: End to end carbon/water cost - No one knows how to authenticate most of that or what's acceptable. It's all made up anyway, nobody actually knows the energy costs.

Tristran: Also made to be able to trick people. "Green energy".

Sarven: which is why getting a hold of the source data, how it was generated - the provenance is important. As I've mentioned something like the "oh yeah?" in the initial TAG meeting web arch / commons.

Jeffrey: would like tos ee the sustanable web provide guidance about how to estimate energy and water costs. We need someone to write that down.

Tristan: it's only a part of the equation. Facebook renews their servers every 2 years.

Amy: even more complicated.. if you're replacing it with a more efficient server..

Jeffrey: in terms of accounting for the cost you can say it used x amount of time on a server we used for 2 years..

Tristan: servier itself has ac ost of manufatcturing.. air pollution.. water pollution.. hot water.. explodes in complexity..

Jeffrey: being able to list all those aspects would be useful... at the end you could collapse in a number. But for the standards related stuff keeping them separate is fine. Your data center uses some mix of stuff for each request, but your webpage is going to call out to a number of different services. You only need to evaluate them at the end

Amy: if that happens in the user agent you're not getting the problem of websites using out of date metric calculations

Amy: There is a conflict of interest. e.g. Google is providing the data centres and then the footprint of the browser. The stuff is too hard to fit into one person's brain when they have so many other things in their mind from their lives.

Jeffrey: re Supply chain stuff, I was always worried about auditing..

Amy: There is a complete tunnel vision. We write down what's in the box and recorded and therefore must be true.. but what if all the things that are not accounted for.

Jeffrey: passing data through..

Sarven: what's the use for end user? A report might be more useful?

Jeffrey: different for different websites.

Sarven: certain services can predict how much it would cost to run eg a query

Amy: what recommendations are we making to Sustainable IG

Sarven: maybe wild idea: have the browser cap what they can use per day

Amy: this would be easier if the data was available

Tristan: complicated because of differences between build, use, waste... lifecycle assessments

Amy: security updates.. something we can do about that?

Tristan: regulator suggestion for separating security updates from feature updates

Jeffrey: for me, lifetime is how long the provider is willing to provide OS updates

#### Potential steps forward

Recommendations to IG:

* Websites should present information - several indicators - about their use of each kind of resource (e.g. carbon, water, minerals, SB-equivalent (earth moved to get mineral), energy) to the UA, so the UA can show the user (or do other things). Recommendation is to focus some effort into making this data available end-to-end.
* Focus on recommending a calculation, rather than waiting until we have the perfect calculation.
* Focus on what they're the experts on and delegate/collaborate on the other stuff. 
* Prioritising their efforts. Focus on things there isn't another group for. Sort things better by scale.
* Can they provide clearer overview of sustainablity impact across different standards groups?

Things the TAG can do:

* Factor sustainability into reviews ("triple bottom line" style?)
* Connect Sustanability IG with different groups; enable SIG to educate other groups on the scope of the problem(s)
* Support sustainability IG to develop such that we can feel confident to send people to them to discuss sustainability impact (and have a constructive outcome)

## Digital Credentials

Scribe: matatk

[Draft document: 'The Web Must Never Demand Your "Papers"'](https://cryptpad.w3ctag.org/code/#/2/code/view/6-e78no3AsNb-PNq8CQMaMvtDH5EN+OSzuTsjdxsmHk/)

Dan: Background. Just went through situation where there was a FO against adding digital credentials into the FedID WG charter. In this context, digital credentials means government-supplied digital credentials. The type that people seem most keen to talk about is digital driving licences. My understaning is this is driven by regulatory pressure in the US and EU.

Martin: There are different reasons in the different jurisdictions.

Dan: You may've seen in the news that phones can be used to present these creds. This is about exposing the same info to web sites. The use case that came to mind to me, as a frequent traveller to Japan, would be to provide the info to Japan Web (the app that gives pre-clearance for travel to Japan - it's a web app). Passports are another kind of DC that are not being discussed yet. This is what the WG was propsiong to work on. The council was formed and agreed to deny the FO, so the WG can go ahead with this work. But the meat of the FO which I am presenting now, still stands. The council agreed with the concerns around increased sharing of personal data and centralization on the web. *Other concerns listed in doc* - these all relate to our work on privacy and societal impacts. Also dual nationals should still be able to choose what information to share, and we should all be protecting against overreach.

There was another conversation we had last year about how the UA should be playing a mediating role here. One thing TAG could do is to reinforce the importance of that architecture. Therefore there is some chance of the UA ensuring that the user has agency.

Tess: It's important to point out that that is in tension with the desire to have more decentralized solutions in this space.

Dan: I thought it'd be useful for TAG to do a finding. Findings are one point in time, one opinion, what we think. I think it might be useful to do that to explain what the TAG's views are on this. People may've read the council's view, and even though TAG members were there individually, I think we should do something to represent TAG consensus. An explanation reiterating the points of the council report, and then talking about in particular we believe the addition of government DCs to the web has great potential for harm, so as they contineue to develop this tech they need to consider societial impacts and put in normative requirements to mitigate these impacts.

E.g. the web should not become a platform that demands your government ID in the course of its normal operation. That would have all sorts of bad effects. If DCs are to become part of the web, we need to put them in a box, to mitigate against the misuse and overreach, and all the ways this could be create a negative situation. We need to align with the user's needs (priority of constituencies). Focus should be making things eaiser for the users.

*Highlights the paragraph about the UA providing a central mediating role*

Coming back to some use cases.

* The one mentioned above re passports.

Ideas for requirements/issues they should be considering that they need to create mitigations against.

We were all there on the council and agreed, but have concerns.

Matthew: Didn't Simone do a threat analysis?

Marcos: Yes, already published.

Jeffrey: More such work needed though.

Lola: Centralisation of trust on the web - what does that mean practically? Does it mean that it's going to align more with browsers?

Martin, Dan: Governments.

Dan: Consider a situation where you want to buy a coke from a vending machine and have to provide ID.

Martin: Something like this happens in India (not to that level, but to interact with some businesses, you have to provide ID).

Lola: How does this differ from having ID to buy alcohol?

Martin: Once it's digital it becomes accessible to a bunch of digital systems in a way that was not possible if you're just showing a driving licence to a bouncer at a bar. Concrete example: In Australia, some bars have been forced to implement stronger ID protection measures (as the bar is on probation for some reason). Companies have provided systems to collect this info, and it turns out they're selling it. They state with aggregation, but it is not good. Overreach. The technology exists to _not_ have a system that operates that way, but nobody has deployed it.

Tess: And for the bar case, it's just for age verification. They don't need any more info.

Martin: They need a photo and that you are over 21 or what have you.

Amy: They only need to know you're older than a certain age.

Martin: Standards that could solve this have been proposed but not deployed.

Yves: A system that could simply scan and recognise you.

Dan: We could say that the entire DCs space is wrong and needs to go back and change to a system where only the required info is provided.

Martin: That's what EU law says - purpose limitation; information reduction; unlinkability (which is hard).

Peter: In the case of drinking - the one bit we need to verify is that you're over the legal drinking age. This is the wrong thing - we should be checking you have the right to alcohol. E.g. someone with many DUIs could be prevented.

Hadley: Is that law in any state?

Peter: No but if we're going to lift this system we should do it corretly.

Martin: Some ID providers have put out papers on such issues, stating it's more complex. But it is down to their commercial interest.

Dan: We could do both things - say that TAG thinks the architecutre should be this (matching EU privacy law). And we could also say that, given you're not going to do that, but build on something already on people's phones, here is what you need to do to mitigate the harms - because of the ubiquity of the web, that it must be safe to visit a web page. This is much riskier than using a native app; it has to be more safe. Can't just take the same native device use cases and apply them to the web.

Xiaocheng: When thinking about threats that could be introduced by gov-issued DCs, what are the bad actors that we are considering? We talked about gov or regulatory bodies. Anything else? Second question: comparing this to more traditional forms of verification, e.g. logging in with a Google (or other) account to verify identity online, what are the differences?

Dan: My immediate answer to second point is it's about centralization - it's easy to identify with GitHub account instead of Google, or an email - so it can be replaced. In the first point, who are the bad actors? Re my notional use case about dual-nationality person showing up at a border, it's the overreach of the national authority that's the bad actor. That the national authority would want to know that someone has both citizenships even though that's a perfectly legal status to have, and they aren't compelled to give all the info.

Hadley: In some cases you may have to show all your citizenships, depending on where you are.

Dan: If it's the law where you are visiting, yes. But not everywhere, and shouldn't be compelled to give the info if not requried. Comes back to data minimization and purpose limitation.

Tess: Re multiple passports. The US government requires US passport holders to present their US passport at the US border. If you have another one, they don't care, but it's illegal to present a non-US one if you have one. Currently you can do this physically, even though it's illegal. You can imagine the UX here, the UA will be tryig to help you not break the law. However, it's reducing your agency. Your device shouldn't violate the law for you, but it should be your decision.

Martin: I don't find that example compelling. I find Spain concerning. They are building an age verfication system for accessing porn. It's a surveilance apparatus.

Lola: Same in UK

Martin: Similar is being developed in Australia. The problem is how they are implemented. They _could_ be unlinkable, but they are not. Which means the government can compell them to get a list of all the users and activities.

Hadley: In the UK they are talking about having third-party providers to handle this and collect the info.

Yves: Thus you (gov) will have less intermediaries than sites to check for this info.

Jeffrey: What to get out of this?

Hadley: We should separate the ethical and legal from technical. Lots to say on all, but technical is where we could make more progress.

Yves: We have e.g. the Data minimization principle in the design principles. So the discussion could be about that. The angle.

Martin: Focus on surveillance. Applicability to use cases. Many reasons you may ask someone to present a DC and some are perfectly fine, and some are totally not. Will reuqire different tools for different use cases. Also focus on requirements in EU legislation that the person requesting digital identity authenticates themselves and has the right/authorization to access the info - this means that these can be logged and inspected.

### Digital Credentials Breakout

Present: Tess, Martin, Marcos, Lola, Dan, Yves, Matthew, Xiaocheng, Hadley
Scribe: Matthew 

Dan: Should we write a finding?

Martin: Yes, start is good, more places to explore after.

Marcos: Yes, division of labor needs to be discussed.

Dan: Happy to get input - my experience comes from the council activities mainly. Let's focus on what should be in the Finding.

Marcos: We will need to come to a shared understanding.

Martin: I'd like to root this in the use cases. Flat-out issue of government credentials on websites. Giving your entire passport to a website is bad.

Hadley: Giving the info to gov, or 3p?

Martin: EIDAS legislation has provisions that only authorized entities gain access to the identity. Concern about how well this will be implemented.

Hadley: The case you're talking about: I have gov-issuesed creds - are you talking about the case wehre I'm giving them to gov, or some shop, like a wine store.

Martin: EIDAS covers both cases. If you want to break it down to that next layer (minimization) - gov ID for gov services makes some sort of sense. Gov ID for wine store has some things. Gov ID for cheese store is a simpler case. When we get into age verification, we have a whole class of stores/services that might need that. Gets into selective disclosure etc.

Dan: We should keep in mind that what we write in a finding should inform the activities of a WG. Marcos can help us to ensure that whatever we write will be useful to that group.

Martin: *re diagram being set up* Issuer, Verifier, Holder?

Marcos: Actors: Issueing Authority; Web site (relying party); User.

Some examples of sites may include age verification, or proof you can drive.

Parts include: Standard for how the issuing authority requeststs information; selective disclosure. There is also a governing authority - larger potential regulatory body/authority that covers what info can be disclosed and accessed.

*Shows example of digital driving licence, which doesn't work - highlighting a risk in the system.*

In the selective disclosure case, I want to go to a nightclub and don't want to share my name with the bouncer, but I can show a QR code that verifies my age. Similar codes exist for different situations, e.g. police stop.

Lola: In the case you got pulled over, and had done selective disclosure, can they see that you have done the selective disclosure?

Marcos: Yes, you can provide a credential that says you are authorized to drive.

Dan: About always having to have a physical as well as a digital credential. Could we suggest a mittigation to the WG that sometimes this system should not work - just like logging in to your laptop with biometrics, sometimes you have to type in your poassword. This proves you know and remember your password. Should this system should work the same way, such that tehre's always the option to use the physical credential?

Marcos: Similar to if you have a phone that unlocks the door to your house. If your phone runs out of battery, you have a backup key. This is also in the device but runs in a very low power mode. Whether the alternative is physical or not, it's a well understood problem.

Lola: I would like to explore other alternatives to address the issue Dan mentioned. I am cuatious that over past 15years so much has become digitsed and user behaviour has changed. If we introduced something where _sometimes_ you have to present physical ID, it could become very inconvenient for users, e.g. if they get stopped by police and don't have it when they need it, this could be problematic.

Martin: The police need to have procedures for this. People may've come from other states/countries. So you already need a system to deal with that. One of the problems with soem of these systems is they don't recognise these possibilities.

Lola: I agree, however, especially when it comes to authorities, it's easy for authorities to use those things as to why they have prejudiced a particular person or group of people.

Martin: agree

Lola: Maybe outside our remit, but if we can limit this, it would be good.

Hadley: Want to focus the conversation: sounds like we're trying to design the system.

Marcos: *to diagram* Regulation, standards - from W3C we have verifiable credentials. There's some sort of cryptographic magic that happens

Martin: digital signatures

Marcos: Each system has different qualities. There are a number of different standards. MDOC by ISO. Open IDP by the Open IDP foundation. VCs by W3C. They all provide slightly different things.

Where W3C comes into play is when we talk about the user, which Martin raised ealier. If we make this easy to use, people are going to (over)-use it.

Martin: supply-demand economics; if you make it cheaper, you unlock latent demand in the system.

Marcos: Everyone loves the \*Pay systems - they're easy, and attractive to users.

Various of us have experienced a variety of system to try to verify that a passport is correct - e.g. one that flashes colours in your face to ascertain that you're a 3D person and not a photo. Problem needs to be fixed.

W3C comes and wants to use a URI scheme. e.g. 'wallet://unbound string of any length' - this would open a wallet. But what if there are two wallets that claim this URI space?
  
Tess: How do you get back to the web page after this?
  
Marcos: There are lots of problems with this approach. W3C proposes an API that takes these things and UX into consideration. Includes all the regular things we put into web APIs. E.g. needs user activation; secure context; credential management; ...
  
Xiaocheng: Which party controls what to disclose?
  
Marcos, Tess: That's the key question.
  
Marcos: E.g. government says all porn sites must be registered. With MDOC, there are different classes of web site, and it might say "you should ask only that the person is over 21" but other classes exist where you can be allowed ot ask for more info. So this is a weak link in the system.
  
Martin: This is where the EU legislation says that you have to have a legitimate reason and be authorized to access the info.
  
The issuing authority goes two ways - (1) to your wallet and (2) to the website, which has to present something that verifies that they are authorized to access that info.
  
Marcos: This ensures that it's cryptographically verfieid that only the reuqired info is provided.
  
When the trusted UI comes up in the UA, it says "here's the thing it wants from you" and you can accept/decline/choose what to offer. It may then be accepted, or rejected by the site/service.
  
So this gives either real or illusory selective disclosure.
  
Martin: it's all an illusion
  
Lola: What about a business that has multiple sites - e.g. amazon.com vs amazon.co.uk ?
  
Martin: TBD
  
Hadley: Sounds like first-party sets
  
Martin: QUAC - Qualified Website Authentication Certificate. Hasn't been fully decided yet.
  
Marcos: You have an ifrmae and can contact the issuing authority from the iframe.
  
*everyone is really into this discussion (rightly so!)*
  
Dan: Where can the TAG be impactful?
  
Marcos: We're saying that not everyone can participate in this system. In order to become a registered DC scheme on the web, you need to meet the high bar of criteria that W3C has.
  
Martin: What would those critreia be?
  
Marcos: Exactly.
  
I made some suggestions. Revokable probably not going to be a thing. Selective disclosure. We could build on this.
  
Hadley: E.g. if issuing authority is EU, could the IA say "we will only deal with MDOCs, or W3C VCs, ..."

Marcos: Yes, that decision is up to the IA.

Hadley: but the browser has to be able to deal with all
  
Tess: Browser-wallet combination
  
Dan: Has Open Wallet Foundation come up here?
  
Marcos: Not heard anything from them.
  
Martin: have had conversations with them.

Marcos: Have talked with e.g. Google, OpenID. When you take a Web IDL definiton... in Google we may pass things to the OS. WebKit is different, strips everything out first. Gecko may be similar to WebKit.

E.g. MDOC has two properties which are base64 encoded.
  
Architecturally you need to be able to verify that what you're sending through is safe; need to say who has to do that, and what to do if you find something that's dodgy.

Martin: Looked into OpenID for VP. At a high level, website says "I want an OPenID for VP" and the UA passes it on to the wallet, which looks at and fulfills (or not) the request.

In the EU model, where the site has to prove it has access to that info. The website says "I need to access this info; if you want to check I'm authroized to do this, here's a URL you can visit", which the UA passes directly on to the wallet, which goes to the URI. Then when it visits the URI, all the controls that teh UA might have applied to that request go out of the window.
  
Marcos: We got rid of that part of the approach.
  
Martin: There is an attack here.
  
Marcos: The user's ID can be encoded into the string.
  
Dan: What are the high-level statements we could make as TAG, that as you design this system and make these checks and balances, and implement them in a W3C privacy compliant way, here are the architectural precepts you should be applying. We can point to things that we already said in design and privacy principles. There may be other things too.
  
Marcos: We used some of these already. E.g. ISO wanted iso.org.mdoc but TAG guidance is "don't put dots in your enums".
  
The versioninng thing: some wanted to put versions in there. We had to push back on this.
  
Tess: this is an exmple of guidance and mentoring that we have to provide to help people work in this space.
  
Yves: Can we avoid the custom URL scheme?
  
Tess: Yes thsi is one thign on whcih we need to provide them with advice - and we want to help them do this right, so they don't go around it.

Martin: using HTTPS at the start is still a problem as it immediately allows all of the protectiosn we put in place to be subverted.
  
Dan: What can we put in in order to avoid that?
  
Lola: Who is this for? Impelementers, IAs?
  
Tess: Primary audiene is this working group doing this work. We want to guide them to a good solution.
  
Dan: As they get pushback on that, they can use the TAG's documents to back up why a given approach is needed.

Tess: People creating policy in this area, or any number of implementers, they could be pointed at TAG docs for guidance.
  
Lola: In which case the privacy princpile about de-identified data could be valueable. Not clear whom the 3p is - is it the IA? But if we include in our finding about de-idenfied data, they want the IDs. They want to know how many bottles of beer someone bought. To what extent do we advise knwong tht some of these people are policy makers and will disregard?
  
Marcos: We can only make recommendations - you identified a key aspect.
  
Martin: I think we should concentrate on putting users in contrtol - point to the examples _in the EIDAS regulation_ that requires that only the required info must be sought.

Marcos: The challenge we can put is that if an org wants to register, they need to meet the high bar of privacy. Not sure we need a finding.
  
Martin: But having a TAG finding adds more weight.

Dan: Do you object to a finding?

Marcos: No

Dan: if we're going to do this work, we may as well do a finding.
  
Martin: There are more audiences for this.

Dan: We didn't with first-party sets, maybe should have. This seems to have lots of potential audiences.
  
Marcos: prioritise the data format, request format, that part of the architecture.
  
Tess: The finding should contain guideance that the WG can apply to criteria for inclusion in the registry. TAG can present the view of the community as a whole as to what the bar is - if a scheme doesn't meet the bar, the WG can't put that across on its own - this is where the TAG can have the most impact.
  
Marcos: We don't need to focus on things like verison numbers - the bar is the most important part.
  
Martin: Agree - you are handling the version numbers and other issues in the WG.
  
I think we need to start with background context, then use cases. Why do people want to present DCs online?

Marcos: the spec has a whole set of use cases.

Drivers licence, passports, student IDs. We can go from there.
  
Martin: We can point to those, but want to clearly state them and why they differ in different contexts.
  
Marcos: raised a good point; for some gov sites you can log in with a Passkey (don't need a gov DC). A problem is pepole wanting to use DCs to log into web sites.
  
Martin: two things apply when using DCs to log into web sites. 1 is sites that, by law, need to know who you are (duty of care; regulation). If you're looking to buy cheese, there's no regulatory requriement that your identity be known.
  
Dan: Can we say they should never be used for login, but only when registering, if they need to be used?
  
Martin: There are regulations in some cases, e.g. in EU, VLOPs (ver large online platforms) are required to optionally provide EIDAS based authentication. At reg time perhaps, but if you register with it, they have that info.
  
Peter: It's a harm reduction though, because if at reg time, they get what they get, but if on login, they can get more eaach time, and you can protect your gov DC. You could keep it offline.
  
Hadley: Less over the wire, too.
  
Dan: A wallet should never be needed to log into a site.
  
Tess: It would be nice if we could say that, a user account's profile info, once populated, should not get overrwitten when you present a DC.

Yves: What if you want to sign on using your wallet, and you have two devices?
  
Martin: there are standards for that.
  
Marcos: +1; this can work.
  
Peter: across different OSes and browsers?
  
Dan: Could we also enumerate abuse cases?
  
Marcos: Speaking of - everyone wants to use this for payments. E.g. presenting wallet for both ID and payment at the same time.

*Group discussion about anti-patterns, including the use of the DC for auto-fill - the user may not want to disclose certain things; they may not be accurate in certain situations. E.g. when moving house, for a time some details will be out of date.*

*Group has apparent consensus that ideally it should be technically impossible for these anti-patterns to occur in practcice. Most people don't consider the nuances of a person's identity and details, so we need guidance, normative requriements, and architecture to assist here.*
  
Dan: Could we put things in like rate-limiting for requests for DCs?
  
Xiaocheng: We should make it normative that DCs should only be used for identification and only when needed, so _not_ autofilling a form. I am still thinking about which party controls what's disclosed. E.g. I'm a bad actor and want other pieces of information. We don't want a situation in which some actors are gaming the system to gain market advantage.
  
Martin: If you're doing age verification anonymously. Hard to build that system becuase you don't want to indicate that your licence was issueed by the Californian DMV, rather than a French similar org. But it is possible to build such systems, even though none has been deployed yet. But if this happens, Yves could generatr that proof and sell it to anyone. So we need to build rate-limiting in as well. Once you have all that in place, you naturally have all the necessary controls to ensure that every single web site could ask this question and giving it to them would cost you nothing. There's no privacy loss, but we don't want that situation. Once the tech is in place, it becomes that much easier to ask.
  
Yves: you takled about French driving licence signalling you're over 18. Actually it changed and now it's 17. So evertying that was coded on that assumption will fail.
  
Martin: This ties back to Peter's point that you want "can buy alcohol" - but that depends on where it's being purchased.
  
Peter: So even if the signal is "I'm allowed to buy alcohol" rather than "I'm of teh age" it depedns on where you are.
  
Martin: All of this can be done with zero-knowledge proofs.
  
Marcos: Google is trying to put this in to the MDOC spec.
  
Martin: I think this is a mistake as the system they're building is massively computationally complex.
  
Marcos: They claim they've got it down.
  
Martin: It is limited in its expressibility.

Dan: We have started to wind down.
  
Martin: We have enough to start on something.
  
Marcos: We have the beginnings of a set of criteria that all of these different schemes MDOC, ..., must adhere to.
  
Hadley: Looking forward to seeing the draft, focusing on what's architetural.
  
Marcos: Having a document that allows us to have a say in this will be helfpul.


## Feedback from Sustainability 

Scribe: Sarven

Jeffrey: We focused on - while weren't getting distracted - what the IG can do for the web to move forward looking at the se problems. re Potential steps forward: the ideas... website should be able to present info broken into each kind of resource. The guidelines should present to UA various use of resources, showing whatever is useful to the user. the IG should focus on getting websites from E2E.

Amy: With the caveat that all these numbers come as approx.

Jeffrey: Getting something out there is recommended.

Amy: if it ends up in the UA, in terms of a score or whatever, rather than delegating to the website. If we can put some of that to the UA, expose it that way.

Jeffrey: The user may have prefereneces on how to calculate the score.

Dan: For instance, JSON in a well-known location?

Jeffrey: or link header, other discovery and expression

Dan: Interesting to contrast that with carbon.txt coming out of greenwebfoundtation. Not focused on data actually but here is a link to a sustainability report and stuff like that

Jeffrey: so this is not doing carbontxt. we're saying dont do that. do sometihng different

Amy: depends on UC and circumstances

Jeffrey: If user sees this than they have the ability to choose the website or whatever axis they care about

Dan: When I use iOS I see screetime report, that tells me about which websites I used, how much time etc.. So analogous to that and do nudge user's behaviour

Tristan: we are energy blind - spending on running and the network, also other consumption. THis could make it visible in some way, but at least making the mechanics to the user to make informed decisions about it.

Marcus: school of thought on putting the action on the individual. but what is the energy impact of each spec. when i open a gov webpage burning a lot of stuff down, i dont have so much choice or do something about it. we can identify some things, e.g. don't use x, but there is a balance in user reports and what does that mean, and how to impact at scale of consumption on the web

Amy: the base line is that this is necessary - easy to talk about - but not in competition with highlevel movements, corporate. Can address in multiple angles, not an either or.

Matthew: All of this stuff is going to be gathered on best effort basis. In future, how these numbers are accredited to people.

Jeffrey: These are claimed number and no authenticity behind them. At least in some jurisdictions you may be liable in some ways. Not only can you make these claims but hired an auditer to have a look.

Amy: This isn't just for the end-user. Lots of ways the data could be used in future, e.g. search rankings... and other things we can imagine (or haven't yet imagined).

Jeffrey: Focus their document their expertise is on. They have big section on UX design, but only one security. Should prioritise their effort with the scale of the effort. THe doc is kind of grabbag. Hope that they can provide an overview of sustainability impact across various standards groups.

Amy: The incensitive to do it is not super strong. Looking at where sustainability guidance can factor in.

Marcus: re WebKit Team's with improvements to WebPush, I don't know the scale of th eimpact but e.g. dont spin up service worker. Just saying as a tiny improvement or where you can optimise things.

Amy: There is complexity for DX with the Web platform. Backwards compatibility, less hardware intensive.

Dan: My mind went the WebRTC, for instance, when I use Whereby I can switch from P2P or aggregate, 500 people.. and then you are a lot less energy with P2P. Things dont rely on data centres as much. If they came and said P2P is no longer supported, we can say that's not a great idea and encourage less use of data centres. As Tristan pointed out, data centres is one of those invisible things. Is there something from the spec's perspective to encourage more P2P thinking.

Hadley: Saying decentralised is the way forward?

Dan: I didn't say the D word :)

Yves: The delay between people matters.

Dan: The usage of that centralisation is for signalling rather than bandwidth

Jeffrey: I'd like to hear the IG's on how much energy we are saying by doing more P2P

Martin: If I setup a service where it can ??? there can be a pause without streaming the video ???

Matthew: Didn't Marcos just talk about applying the resource usage stats discussed above to specs somehow? So if there are different modes in the spec, that might come out?

Jeffrey: Most spec authors don't have those answers. It'd be fuzzy to do that computation.

Jeffrey, Matthew: might be nice for this IG to help, if they have the expertise.

Jeffrey: we do various questionnaires and checks, can connect the sustainability group to others, and they can go there to be educated.

Dan: We can encourage the creation of ..

Jeffrey: ... as a horizontal area

Dan: how about post-apocalyptic stuff?

Amy: Sustainbility of the web platform for a set of tech, and using the web as a tool for helping the world deal with any kind of disaster

Lola: Is the sustainability lead looking across various groups at W3C on this?

Jeffrey: re Amy's point on how can the web can help: there are also aspects on being resliant to environemnt disasters, and need to operate more p2p temporarily, like downloading wikipedia. the second: finding ways for scientific communication, all the tech bits are there but it is a social problem, and still deciding to use these expensive journals. all of the publishing mechanisms exists but not using them.

Dan: re apocalyptic web, building tech for people deal with disasters, back when we had the Arab Spring (2011), there was a social web workshop with an Egyptian developer talking about protests in Cairo, and the gov turned off the Internet, and they couldn't use it - even though the website is inside a bubble in Egypt, but because they turned off the tap to the outside world, they coudln't access by IP access. That then the question was and still is, how do we make the web more resliant for that kind of temporing, as well as for other things like the disasters. TimBL asked this as well in a TAG meeting soon after that, and we haven't risen to that occassion.

Amy: This has been happening for years, and there are communities that deal with diasters despite us and lack of support - in a "cloak running things" - if we work on this, we need ot bring people into the room have been dealing with this and take that into account.

Dan: what could the web can do to support you better kind of thing. understanding the UCS, and oh yeah everything should be p2p like bittorent but that doesn't solve everyhting.

Matthew: Yes, and. I think Dom at an AC meeting, it wasn't as much ... is there a workshop that needs to happen that brings people on this?

Dan: Agree. Like NGOs, and not just tech companies - sustainability wash or something.

Jeffrey: Tristan and Sarven will get involved with the IG.

Dan: Talk with Tzviya

Sarven: I am.

Amy: Also mentioend browser capping the user's access to things if they go over

Sarven: So it wasn't a wild idea after all!




## Feedback from Digital Credentials

Dan: We reached consensus that making a Finding is an OK thing to do. Marcos is a little concerned that it might be "preaching to the choir" (the WG) but it has multiple audiences, which includes tht wider community and other standards groups, regulators, ...

Jeffrey: Does this mean we need to write the Finding with the WG?

Dan: Marcos can represent them.

Martin: We don't want to have it look like the WG is speaking through the TAG.

Dan: We talked about a range of scenarios in which DCs could be used for various reasons. Just one example: we want to technologically prevent things like DCs being used to log in.

Martin: e.g. via rate-limiting

Dan: Other areas too...

Matthew: ...stopping DCs being used as a source for auto-fill...

Dan: ...stopping DCs for ID being coupled with payment. All sorts of things where the case doesn't warrant that level of info.

And referring specifically to EU regulation that provides good wording around selective disclosure, data minimization, and publicly available justification for the access.

Martin: You need to separate the use of the credential from the other info that people need to present to sites.

Dan: Abuse cases. Including requsting the info when not really required.. We agreed we have to have a Finding that puts strict guardrails around use of these technologies. The WG will be working on such things, but should some organisation push back on these guardrails the WG can point to the TAGs Finding that reflects the community's view.

Jeffrey: Google has developed some APIs that require registration in order to use. This has met with disapproval from the TAG in the past. What happens here in the case of an API that needs registration with a certain authority?

Martin: Browser can say the user can't access the API in a given jurisdiction.

Dan: Does this scale to the small web as well as big?

Martin: Ultimately this is about governments and very large online platforms (VLOPs in the terms used by the EU).

*discussion about barbers' shop loyalty cards, and bigger loyalty card schemes*

Lola: A barber shop would want to be able to check that a customer is part of the loyalty scheme.

Martin: We talked quite a bit about how age verification case is distinct from others. Within that there are restirctions around the delivery of content, and of services, and how they are different. *See notes above.*

If the goal of the government is to cut off access to certain types of content, limiting only access to commercial outlets will not be sufficient.

Hadley: it's a barrier though.

Dan: Marcos provided insight into how the WG is working, and that they are curious about all of thse issues. I think it's still useful to make this statement that, yes the FO council said it's OK to have it in the charter, it's useful for TAG to make some statements about it.

Jeffrey: I'm fine with us writing this. Generally nervous about recommending things in detailed technical areas in whcih we may know less than the WG. Mitigated by the fact that Martin and Marcos know the area really well. But we don't want to make impossible recommendations.

Martin: I'm aware of some of these.

Dan: One way to deal with this is to anchor the work in the existing documents on Privacy etc. that we have already written.

Martin: This comes down to in large extent a bunch of pointers to the Privacy and Ethical principles, and societal impact questionnaires, with the former two being the primary parts.

Dan: I think we are being asked for this work.


### Breakout 9A: FedCM

Present: Tess, Marcos, Martin, Yves, Peter

Discussed a few FedCM issues and closed them.  Some for being OBE, others for being fine.  Leaving #945 out on the basis of it being still under active discussion.

Discussed AI stuff as a bit of a distraction.  Discussed whether the choice of model is reproducible.

### Breakout 9B: Carousel

Present: Dan, Tristan, Xiaocheng, Matthew

Four specs:

* [CSS Overflow Navigation Controls](https://github.com/w3ctag/design-reviews/issues/1037) - split out in to the following issues
  * [CSS Scroll markers](https://github.com/w3ctag/design-reviews/issues/1053) - not yet reviewed
  * [CSS Scroll buttons](https://github.com/w3ctag/design-reviews/issues/1054) - in review
  * [CSS inert](https://github.com/w3ctag/design-reviews/issues/1055) - in review 
  * [CSS Styleable Columns](https://github.com/w3ctag/design-reviews/issues/1056) - not yet reviewed

Matthew: Some discussion about inert - what do we do when ... how do we generalize this. We don't want people to think they need to put CSS inert on lots of things...  Alice commented recently.

Xiaocheng: Alice [says](https://github.com/w3ctag/design-reviews/issues/1055#issuecomment-2695910757) it should be restricted to top layer mechanisms.

Xiaocheng: My initial opinion was that I wasn't convinced about the use cases and I also had accessibility concerns. Since Matthew & Alice both raised those concerns that makes my position more firm.

Dan: have they responded?

Matthew: they responded about uninert... there is one question I asked about scroll buttons - about how they plan to generalize ... this requires several other features to be implemented first.  This approach has worked well for things like masonry. Right now we are talking about the context of carousels. But we may want to generalize this to other things that scroll. But it seems to work differently from a keyboard perspective. In the scroll buttons explainer - it says the the scroll button can be focused but doesn't have to be focused. It would be good to have it confirmed that they are not trying to change the way scrolling works... They haven't answered that question.

... On ther inert topic, Martin, Alice and Xioacheng all highlighted areas of concern... All valid points. Seems like it could be misused very easily.

... there is about a decade of UX research and advice against carousels. I respect the CSS group's approach to make this less bad. If we can get to the point where it is less bad then that is a harm reduction thing. Not sure if they have yet got the harm reduced to a level where we can be comfortable with it. 

Xiaocheng: background of this work - prior work - stylable select - this work is incubated in OpenUI group. They have done a lot of studies on standardized and accessibile versions...  A general design seems complicated so... they want to indentify common parts. Regarding select that's pretty much done... Custom stylable select with pure HTML/CSS.

Matthew: that work is good... 

Xiaocheng: working to identifying common components without a general ...

Matthew: the challenge with carousels vs select ... select is an element. Narrowly focused. If you make a carousel, it can include text, videos, buttons, ... each with ARIA tags... loads of different components... My concern is : they are doing fundamental building blocks but do they intend for this scrolling stuff to be used for scolling in general? They haven't answered the question about the scolling stuff.

*we review Matthew's pevious feedback on scrolling*

Matthew: they specifically said -that the reason they didn't do it in tab order... is that what is what the ARIA guide recommends... which is true, for carousels. But if inert is being used outside of carousels, then will it also be used in this way?  We left this feedback.

Xiaocheng: this leads to some more design questions... stand-alone features that can be used outside of carousel. If we work on carousel first and theyse parts become internal parts of carousel .. and we expose more specific / safer / restricted API.

Matthew: yes and if you want this behaviour - content not focussable - there is a technique for this already -use tab index of -1..  If it's only going to be used for carousels then maybe it should be done that way.

Dan: could we bring someone in to help?

Matthew: I'd like for us to ask Robert and team to come and talk to us about the proposal, the context, and where they see it going in future. I think that is the best first step, so we can understand where they see these things being used. Personally don't think it's a good idea to invest loads of energy into e.g.. a new lement for carousels, as they have UX problems (but do apprecaite that CSS WG is trying to make them less bad, and more efficient). Would like to see where the proposer thinks this fits, and where it's going.

*We agree to invite Robert to Breakout B*

*[Posted comment to invite Robert](https://github.com/w3ctag/design-reviews/issues/1037#issuecomment-2697802236)*

Xiaocheng: Stylable columns... 1056

Matthew: the cards ... / slides ....

Xiaocheng: yeah. This proposal is pretty isolated. Targeting the multi-column layout... CSS multi-column layout module.  Only exists in multicolumn containers. This is the least contraversial one... Even without carousels it may be useful.

Matthew: To my mind, a a carousel consist of slides that might range from images to subtree of the DOM... but the designer says "these are the things I want to be on this slide" - but in this case the browser would split things up into slides.

Xiaocheng: In their use case they create a multicolumn layout... 

Matthew: how do they know what will be in each column.

Matthew/Dan: E.g. the cards could be for special offers for holidays, each one being about a holiday to a specific place, e.g. Shell beach.

Descrete regions for offers e.g. is a use case. But can't imagine that the sort of person who wants to create a carousel will say "don't mind how you split the content up".

*doesn't seem to be in the explainer*

Dan: We need to query what the real user need is here.

*guest star Tess on her way out the door*: also agree that this doesn't seem to make sense.

Xiaocheng: Scroll marker: attach a marker to each element ... to indicate progress e.g. or in use case they provided .. and "atom number" attached to each item. Also the scroll markers ... they defined a concept of "currently active scroll marker"... if it's displayed on the  top... They also mentioned about tab index which I don't fully understand the purpose. 

Matthew: they said they explored a range of carousel designs... One of them is a slide deck ... which I didn't think of as a carousel... That's interesting... 

Matthew: In some cases if you only have a few slides they use bullet points of a list to style ... this is the number of slides there are.. If you can use the mouse and can see then you can select one to look at. The information you can get is what slide you're on and what other slides there are... if you do it this way then there is a bit of loss of functionality...

Matthew: we are looking at 2 types of caroulsel.. one is where each card is one thing - one image, and one where each card is a [bunch of stuff]. You could have a list of cards... region landmarks... you'd have to make sure each one had an appropriate name.

Dan: concerned about complexity - do we need a new thing or can we use an existing...?

### Breakout 9C: Permissions Policy for iframes and Device-bound session credentials and something something report only mode

Present: Lola, Hadley, Jeffrey, Sarven, Amy

#### [Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052)

Hadley: Why can't keys be exported from device?

Jeffrey: by default they want to use a Trusted Platform Module (TPM) but not everything has one. This API ca be implemented by something that doesn't have it. If you have a TPM you get stronger guarantees than if you don't. Evenif you don't have one .. the browser does its best attempt at making the key non extractable. Sticks it in whatever the OS provides, maybe can be pinned to the application. If you ahve the extra assurance then you get it.

Hadley: better than status quo but.. good enough? Second question.. in goals, first sentence explains the threat model. My assumption had been that the threat model is that the cookie is removed to another device and used nefariously. The goal in that pagraph is they're concerned about an attacker tampering with the UA, browser memory, secrets on disk

Jeffrey: if you have an attacker that can mess with the ua they can copy the cookie and take it somewhere else. Even if you clean your local machine they still have the cookie

Hadley: that's the threat model I thought.. but they don't say anything about cookies removed from the device

Jeffrey: I think that's what they mean by cookie theft.. but they don't define that. I think tha'ts what they mean.

Lola: essentially tmp bound to the device is acting as the authenticator. THe TPM can have multiple session keys? Each session has a key. It's a one-to-many relationship between a session and a TPM?

Jeffrey: yes. Two kinds of sessions here... you log into your website and store your public key with them and that private key sits i nthe tpm, is not extractable. There's potentially a very long session with that private key. A whole bunch of short sessions where you can ask for a short lived cookie from them. Sign a rqeust with the private key, get the short lived cookie backand use that for actual website interaction. It expires and you have to get a new one.

Lola: are there specific concerns you have about this?

Jeffrey: two angles. One that Hadley was poking at - not everyone has a TPM. I believe they're plannign to provide the api even for the people without the TPMs. THe guarantees only apply to people with TPMs. Is this actually going to be able to improve the ecosystem? Google wants to use this to get better assurance for everyone. Google already does generally good things with session lengths. WHat I'd like is for the banks to accept longer sessions. Is there any prospect of this api improvig that? We should try to help the users.

Lola: How does this benefit the user? Understand the bank thing... but people will be fine. What is the benefit to the user of this specific thing aside from the security thing? Or is this mainly addressing it from the security perspective and there is no tangiable benefit to the user?

Jeffrey: it's entirely a security feature. If you run malware and they steal your cookies and you clean your machine, can they still use the cookies? Right now they can, and after this they can't.

Sarven: what's specified? The API between the browser and the TPM?

Jeffrey: between the browser and the server.

Lola: in the first section it says that it offers an api for websites to control the lifetime. This also has a protocol for periodically and automatically providing possession of the cookies to the webistes. It's addressing two things to solve the one problem?

Jeffrey: I'm not sure I Like that division of the two bits. I think of this as the website can register a private key with the server, between the browser and the server, and theyc an use that to issue cookies, which guard general interactions with the server. You get the higher assurance of a private key and the convenience of cookies. Server frameworks are written assuming you use cookies to authenticate, this allows that same pattern.

... The other angle we should think about is whether this could be better integrated with webauthn which is the other api that allows you to authenticate to a server with a private key.

Lola: been xplored?

Jeffrey: talked to them. THey don't think it fits. Webauthn is a js api not an http api. To do most authentication you need something to put it down to the http layer .Second, the webauthn in browsers now calls down to os apis which never implemented the silent mediation option in credential management. If you call the OS api it's always goign to ask the user to confirm. You want a silent confirmation that you still have the key. Martin seems to strongly think and I kinda think we should just fix the OS APIs. But it's true that's a heavy lift. We can't just do that in browsers and it will take a lot longer than shipping this.

Amy: why not both? is this an interim solution?

Jeffrey: don't know. Don't see an immediate path for retrofitting it.. if you get silent mediation instead of asking the TPM you could ask the webauthn key. Probably works the same way. That might be a good answer to my second question. Overall API seems relatively sensible to me. Maybe not phrased the same way as if you were thinking about it as exposing web authn to the http layer, but it works fine. Getting cookie refresh to work better just helps users on its own. If a website is using this t would never have to bounce through a reauth page.

Lola: comes back to how long the session is. Not having to keep reauthenticating that is a benefit to the user.

Hadley: unconvinced it's worth the disruption. Not sure that's a TAG position. GIven that it doesn't cover all users, and some of the reason to do this is regulatory. Regulatory is likely to be if it's not going to cover everybody assume it's not there at all.

Jeffrey: maybe only provide the API when it's useful for assurance. When a bank tries to use this api and it fails, they know they have to reauth all the time. If it is presence they can trust the user has the higher protection for their keys and therefore can have a longer session.

Sarven: transition to a higher secure channel? They said it's widely deployed..

Jeffrey: they also say 60%..

Sarven: assuming everyone is going to have this possiblity, you can migrate away reauthing the session frquently.

Jeffrey: if everyone gets some sort of hardware key protection, which seems like a good thing for hardware to start having, eventually maybe everyone can use this. Nice because it doesn't have attestation. A UA that .. in the long term when 99% of users have a TPM and websites start being written to require this instead of use it when it's there UAs can also implement it without a TPM. WE're not going to build a world where some users are excluded assuming UAs have that work around.

Amy: something device obselescence something something

Jeffrey: reason to do the emulation now. Banks will not trust this enough to give longer sessions. Is this a regulatory thing, or just banks not understanding web security

Hadley: Both. Heavy layer of this kind of regulation that came out of the subprime mortgate mess. The regulatory response int he uk and us was okay banks we gave you too much rope and you hung yourselves, we've got to steop in and supervise more. Also strong motiation for banks to limit their own liability in how much fraud they're exposed to as they lose money. US regulator moves a whole lot more slowly than the UK regulator. THe ways in which those things are expressed is different. Other jurisdictions are available.

*rant about banks*

Hadley: different kinds of login. Once i"m through the initial attaching login credentials to my account which requires all of this, then it's just a 2f username and password login process. IF you're setting up a transaction...

*more bank ranting*

Hadley: more fraud built in to US banking system..

Lola: if this is implemented in all browsers widely, do developers need to do anything different to make it work?

Jeffrey: they need to implement this endpoint that sets things up and does the refresh. They have to kick it off in the first place somehow. Return this session registration (JWT). Their average page is not goign to have to change because of the short length cookies. And they can probably simplify their site a little bit because they can kind of guarantee those cookies are around. You're not in the middle of asssion going to lose them, it's automatically refreshed.

Sarven: doesn't expand on same origin policy..

Jeffrey: question is whether the cookie it sets can be wider scoped than one origin

Sarven: they are only limiting to same origin?

Jeffrey: I see a \*.example.com which makes me think it's not just a normal cookie.. in scope specifications json... not sure that it actually allows wider scope than origins

Lola: apparently MS are also developing something similar. I don't know if they've submitted for diesgn review. The demonstrating proof of possession in the browser application. This was feedback given by mozilla as part of their standards position. There isn't any comment to say whether or not the editors of this spec have considered..

Jeffrey: there is a reply on the mozilla one saying microsoft moved it to be part of DBSC

Lola: the microsoft explainer still has issues on it within the last week. If they've done that that's fine.

... Is it worth trying to get Apple's perspective? There's a response to Apple's concerns about making the device backup worse. They have questions. When we are doing a design review do we need the other orgs to have their positions already? Do we wait?

Hadley: we're largely giving our opinion

Lola: I'd like to know what Apple thinks in response to this person's reply

Hadley: it is useful to know if there's little support from other implementers

Lola: ask how they are thinking about devices without TPM, or users who do not have access to devices with a TPM.

Jeffrey: how does this benefit the average site, as opposed to the large sites with big security teams. Are we mixed on whether this is good overall?

Lola: I think overall it's a good API. Concernes are .. just because it's good don't know if it should be implemented just yet.

... Is there a scenario where the TPM accidentally loses access to the private keys?

Jeffrey: filling up and dropping oldest stuff? I don't think they do that. If it did you'd just have to log in again.

... We could make the comment that we don't think the concern about backups is a real worry. Okay to log in again if you restore from backup.

Hadley: from a user perspective that's not unreasonable

Lola: if I'm restoring a new device I don't want to it to know about me until I tell it

*resume bank ranting*

<blockquote>

We appreciate the plan to improve first-party authentication by using high-security private keys as the main long-lived session credential with short-lived auto-refreshed cookies to help existing server frameworks work as-is.
  
How are you thinking about devices that don't have TPMs? We are aware that this might be useful in regulated environments like banking. What are the chances that banks could use this to lengthen their reauthentication timeouts? Are there any design changes you could make to improve that chance?
  
We think that expecting users to reauthenticate after restoring a device seems acceptable in this case.
  
Can you explain how this could migrate to using keys from WebAuthn's Silent Mediation, if that is ever implemented in operating systems.
  
</blockquote>

#### [Permission Policy Reports for iframes](https://github.com/w3ctag/design-reviews/issues/1050)



#### [Permission policy reports and Report only mode](https://github.com/w3ctag/design-reviews/issues/909)

## 10a design principles breakout

https://github.com/w3ctag/design-principles/issues/514 - we are working on text. 

The concern from our discussion was that an extension to something that has some sort of bad effect might make it more attractive to use the thing and thus have the bad effect occur more often.  The suggestion was that maybe someone building an extension has an obligation to make the situation better (perhaps by working to mitigate the problem) in addition to building their extension.  There isn't an expectation that someone completely solve a problem (that might be impossible), but incremental improvements might be OK.  Circumstances will differ and we'll have to make a judgment call as to whether the mitigations balance any amplified negative effects from the extension.

Protected Audience is not obviously a good example of this because the proponents of Protected Audience do not always agree that these are negative effects.  A better example might be enhancements to `window.alert()`, which is acknowledged to be bad as a stop-the-world API.  Those improvements wouldn't be acceptable without doing something to make alerting less bad.

<blockquote>
As you add new capabilities to the web platform, do so in a way that improves the overall platform, for example its security, privacy or accessibility characteristics.

The existence of a defect in one part of the platform must not be used to excuse an addition or extension to the defect, which would further decrease the overall platform quality. **Consistency is not a good reason to propagate problems.** Where possible, build new web capabilities that improve the overall platform quality by mitigating existing defects. Do not degrade existing capabilities without good reason.
  
**Do not extend a platform feature that has known defects, without considering how to address those defects.  Extensions could create new ways in which the defect could cause problems, such as by encouraging more use of the defective feature. It is not necessary to completely fix all aspects of a defect, it is more important to consider mitigations or fixes when developing such an extension.**

Parts of the web platform evolve independently. Issues that are present with a certain web technology now may be fixed in a subsequent iteration. Duplicating these issues makes fixing them more difficult. By adhering to this principle we can make sure overall platform quality improves over time.
</blockquote>

Action to create a PR with that, which we can then wordsmith.


https://github.com/w3ctag/design-principles/issues/512#issuecomment-2698168826

We discussed, decided not urgent, left comment.

https://github.com/w3ctag/design-principles/issues/490

Looked at https://wiki.csswg.org/ideas/principles and the linked CSS principles documents. 

Left comment re plans to look at each of the principles and open a new issue for any that might be relevant to bring into our design principles. 

https://github.com/w3ctag/design-principles/issues/556

Xiaocheng agreed to work on this. 

Martin said we have a lot of repetition around jenk, and they could be consolidated. So would encourage not just to add a new principle, but fold existing ones in together.

Xiaocheng agreed.

## 10b Design Principles Breakout

### https://github.com/w3ctag/design-principles/pull/555 - we review and agree to merge.

With Marcos:

### https://github.com/w3ctag/design-principles/issues/481 - we discuss about "powerful features"

Marcos: we started with this thing called feature policy which then became permission policy... We deliberatly chose ... xyz as a feature that is gated on having a poliicy... Jeffrey edited permissions policy and then we started to talk about powerful features... 

Dan: I just want to make sure we're aligned... 

*we look at https://github.com/w3c/permissions/pull/401*

Marcos: a new concept in HTML that got added... that the API has user attention... fully active descendent of a top level traversale document with user attention....  

https://html.spec.whatwg.org/#fully-active-descendant-of-a-top-level-traversable-with-user-attention

Jeffrey: we can't change this one today so suggest we move on to the next issue.

Marcos: let's make it actionable...

Action is for issue 401 - Marcos to fix 401 - possibly with input from Jeffrey. 

### Polyglot formats

https://github.com/w3ctag/design-principles/issues/239

Jeffrey: the sense is ...  a couple angles. When you try to efine a format that can be parsed as 2 different languages it causes implementations to have bugs and tends to cause security problems. Some of the issues are to do wuth the data model of the parsed. thing. JSON-LD and JSOPN. You get 2 different data models. 

Sarven: I think we need to clarify the criteria that make something a polyglot "format". E.g. you can process some HTML and get out some JS, or the HTML part.

Jeffrey: THe core dfn is that you have one format and you expet to be able to run two different parsers (or kinds of parsers) on it, and both be correct. You mentioned that HTML kind of fits this. To some extent the fact that you can run JS or not, or style or not, oes that, but there is one HTML algorithm that gives you a parse tree out of your input. The JS shows up in the data model as a result of that parser, and there are choices after that. It's also expensive to choose to have JS support on/off. What I want to say about JSON-LD is that you can mitigate the problems but it's very expensive. Does that help?

Sarven: Kind-of. I read Tess' comment that you can expresss something as XML or XHTML. It's arbitrary in a way. I understand that's a polyglot, but XHTML in itself is not.

Jeffrey: XHTML is a different language HTML.

Sarven: XML family.

Dan: *references polyglot definition https://en.wikipedia.org/wiki/Polyglot_(computing)*

Sarven: Are we looking at something where it could be processed as either one? How are we running through the check to say whetehr it is or not? When you look at JSON-LD, you can parse it as JSON, but when the payload is using the right media type, it's _intended_ to be JSON-LD. It's not meaningful as JSON, as it is for JSON-LD. I don't think JSON-LD is a polyglot format intrinsically,

Jeffery: I agree that XML or JSON-LD-based formats are not intrinsically polyglots, but when e.g. a JSON document is intedned to be parsed as JSON _or_ JSON-LD then it is a polyglot.

Dan: What are you trying to accomplish by parsing this JSON-LD structure into memory? If you are saying you can parse them as JSON-LD and do all sorts of things with them, and they are intrinsically JSON-LD. You can still parse them as JSON _however_ because this is intrinsically meant to be interpreted as JSON-LD, you can only do a subset of things / have to be careful with how you interpret it. Is that polyglot? I think of it as you have a blob and if you parse it one way, yuo get the same result as if you parse it another way.

Ref wikipedia on polyglot languags.

Here is the same text, but you can run it in two separate interpreters. This is a nuance but could be a dangerous one.

Where we got to last time (discussing with VCs) we got to having guidance around JSON-LD and generic JSON parsers. ***FIXME: Scribe: is this correct?***

Matthew: what about code with documentation - you can get documentation out of it, or execute it - is that polyglot?

Dan: I don't think so.

Jeffrey: Wikipedia says, you have one blob, and you can parse it one way and you get some output. Or you run it a different way and get different output.

Sarven: If you're trying to do completely different things, you should use different media types - this may have happened with the VC, but they moved to application/vc. The proposal is to _discourage_ polyglot formats, right. We need to define the criteria, and then if JSON-LD or somehting else fits that, it can be discouarged, but if we agreed it's not fitting the defintion of polyglot. Again, HTML could also be considered as a polyglot. It is also a question of whether two parsed results are intended to be semantically equivalent, and if so, that's not something to discourage.

Jeffrey: There's a VC data model. It's not RDF, nor JSON. It's the data model for VCs. You get input, and parse it and get the data model.

VC1 said you can parse this JSON, or JSON-LD and get _the same_ data model. We hope the semantics are the same. But it's very hard to guarantee that.

The community did split over this. Having two parsing paths that give the same data model is very hard. It's hard to guarnatee that two parsing paths either give the same results, or fail. If they give different results without failing, you have a security bug.

Dan: Is there a spec out there currently that tries to do this?

Jeffrey: Controller Documents does currently. They were DID documents initiially, and then VC wanted to use them, so generalised them. https://www.w3.org/TR/cid/#context-injection: "Whether or not the @context value or JSON-LD processors are used, the semantics for all properties and values expressed in conforming documents interpreted by conforming processors are the same. Any differences in semantics between documents processed in either mode are either implementation or specification bugs."

Matthew: *questions motivations* Why do we need to be able to parse as JSON or JSON-LD? Is this a DRY thing?

Jeffrey: you might write...

Sarven: I don't think they [vc] meant to have separate semantics... it's just that some just wanted to do JSON. The end result is still the same... So does that fit the criteria... for polyglot? If when you process it you get green for this and blue in another way, then that would be one thing... 

Jeffrey: I think the different processors don't alwasy produce the same output... And that could produce security bugs. They say they are doing schema validation... I havemn't found concrete bugs but I find it hard to believe.

Sarven: I agree. But that sounds like an issue on the spec that is using a format. The data model is the issue not the format... 

Sarven: the spec made the decision to parse it as json or json-ld... it becomes the spec's responsibility to exclude all the issues that would be a problem for the son procesor. I agree a spec could do that in theory. I think what we should say is "if you define a polyglot format then you have to do all this extra work... to make sure you can't write a blob and process it one way to get one ... equivelency ... also meaningful in HTTP level with representations of a resource. JPG or PNG is still a dog. Example with a VC resource... the agreement of what you're getting is equivalent between formats... 

Matthew: if you clearly state "this is supposed to be semantically equiv then have at it, but then it's on you to perform those checks" but to jeffrey's point - if it doesn't work in practice, then we should say something.

Jeffrey: I think we should discourage it because it's hard to get right.  

Dan: Maybe we should not talk about Polyglot because this word has become tainted. 

Dan: proposal to reframe the issue - remove the word polyglot, and reframe it around the issue that Jeffrey voiced - that it's very difficult to get right so it should be avoided... 

Sarven: isolate and be clear about what specifically is dis/en-couraged. polyglot format as a wholesale is not useful without a criteria that can be used. how are the authors going to tell whether they are doing polyglot or not.

Dan: let's remove reference to html/xhtml 

Jeffrey: but I think we should include the JSON / JSON-LD example.

Matthew: Example of source code with comments - you have two separate parsers: one produces documentation; one runs/compiles the code. That's OK. But if you have one piece of input, two parsers, and expect one identical semantic interpretation at the end, _that's_ the thing that (whilst it should be possible in theory) is not feasible in practice.

# Day 3, TAG f2f in Paris

Attending: Hadley, Tristan, Amy, Matthew, Yves, Lola, Martin, Jeffrey, Sarven, Dan, Peter, Xiaocheng

## Session 11. Introing this morning's topics

### Explainer explainer and adoption of features from incubation into working groups (Matthew)

*Matthew presents [explainer explainer slides](https://docs.google.com/presentation/d/1gQW1-D7ZSZ7MJLFLefAmx5Bmvz7_V0KBh2aIzlbIkWw/edit?usp=sharing)*

Martin: Can I just say that the purpose of an explainer that I care more about than "can the TAG review this work" is that there is clear documentation for features, their purpose, their effects, and some of the design rationale.  We are not the only people who need that information.

Martin: I also don't care for the template.  Sometimes work can be presented more effectively if it doesn't follow the template.  The template we provide exists to help people start.

Jeffrey: I like the current template, and I also like that some of the example good explainers don't follow the template, and we should say explicitly that you don't have to.

Martin: yes that's what I meant.

Martin: no we should not merge the explainer explainer with the template.

PROPOSED RESOLUTION: move explainer explainer to a Note.

Dan: *defense of why we might want expainer explainer to be a note rather than informal*

Hadley: sometimes it lands differently....

Matthew: I don't have feelings ... nice if it's a note, but explainers themselves are the more important thing. The only thing that concerns me ... we don't want to make it harder for people to write them... e.g. put them in respec, put them in a certain place, the friction should...

Marcos: It's already burdensome enough to do the spec work... the primary audience does appear to be the TAG.

*we don't come to consensus on the resolution*

### community groups / incubation / how work gets into working groups

*Matthew presents slides from the above deck*

Marcos: i have proposed various alternative solutions to this problerm...  embedding more people... making them accountable...

Dan: I think it's too negative to say that work is happening in CGs "isn't happening in W3C" because they're supposed to be more welcoming to external work that we want to see happen in a more open environment but still in W3C. Need to have a more nuanced statement and not make peolpe feel like the work they're doing in CGs doesn't matter or isn't in W3C because we've sold them on the idea that coming to a CG and you can do work here in W3C, it's just not REC-track work yet. We need to make sure we don't jettison that value.

Matthew: completely agree, respect the success that CGs have been. Getting more peoples views into the system is fantastic.

Jeffrey: seems like there's consensus there's a problem, we should spend time on what to do about it.

### AI

[Slides](https://docs.google.com/presentation/d/16VRt6_OrAjcBTQ0IV3tXgxCX5B6b3sCQi97QAWEooUw/edit#slide=id.p)

Hadley: *presents slides*

Matthew: one of the questions in RQTF is about how AI impacts a11y. Working on an AI document. Complements some of the other stuff. And we did have input into the ethical principles document.

Hadley: ...output qualty including halucinations, etc...
... input sources ... not losing the value of what was used to train ...
... undersirable side-effects e.g. e-waste, power consumption, etc...

Hadley: (a) need other editors to step forward... (b) we still need to talk about what we want to accomplish.

Dan: having discussed web machine learning ethical principles with Anssi, there's an opportunity for us to input into that if it's valuable for the TAG to help. Currently stalling, it has no editors.

Jeffrey: there are harms that the current AI systems have caused .. some of those harms touch the architecture. Credibility of content on the internet, and commons impacts... also sustainability. We should connect the threads.


### User Agents and 

baseline ([slides](https://docs.google.com/presentation/d/1W5F_MHHnAxkwQEimzZ2-A8j1BPeKSU9xuNiZ_hWpXp4/edit?usp=sharing))

Lola: *presents slides*

Lola: UAs aren't just browsers... any software that interacts with the web on behalf of the user. UAs choose which standards to implement. But we need UAs to have responsility for the users. We need to do some writing.

Lola: **High Performance Baseline** lighter user agents, eg. mini-apps. How do do we want to start thinking about div...

Dan: clarifying high performance baseline vs. baseline...

Lola: 2 different baselines.  Baseline we know now is in the WebDX CG.  This is a CG that is more thinking about user agents...

Xiaocheng: introducing CG. Here the basline means a subset of stadard features that are simple enough to implement ...

Jeffrey: my understanding is that this would identify a subset of web features...

Marcos: violation of the one web principle.

Jeffrey: is there a compromise available.

Martin: a very big line between web views / that class of user agents and the mini-app platforms that are being considered. A web view is just another way to use "the one web"... largely... a mini-app is essentially an independent app development platform that happens to use web technologies.

Xiaocheng: Jeffrey's summary is correct.

Dan: It is worth separating that off from the Baseline in WebDX group - that's not the same. WHat they're trying to do is gradually also increase the number of features that are seena s baseline, because they are implemented across multiple widely used UAs. It is useful .. to say maybe you need a new name, this is going to be extremely confusing.

Marcos: we have webperf already

Dan: if they're talkinga bout subsetting web features regardless of whether we think that's a good idea they should be referring to the same list of web features that the webdx group is referring to. They ought to be looking at building on top of the work of webdx rather than going off in their own direction

Lola: I'm not sure they're they web features they're talking about

Xiaocheng: I'm not sure. Features by current major brwosers, mature product. Talking about helping immature products to ...

Dan: concerned about seeing webdx in context that it is talking about features with the same granularity level as mdn and caniuse and other things, documentation and compatibility indexes and tooling. There are things happening that are using the browser compat data, that if you are going to subset web features it makes sense to refer to those features in thes ame way so that at least gives us an opportunity to use the same documentation rather than a completely separate thing.

Jeffrey: discussion of what names to use for the features int he subset gets ahead of where this group is. Marcos raised the important question - is this a good idea at all. It is incompatible with the content on the current web. How would one migrate content to this? Or is it meant to create a separate web that constrains these browsers.

Martin: talked about a number of different things that covered a very broad space - we have the web and UAs we understand. MiniApps fits a very broad definition of UA which is potentially useful to explore to understand where the differences are. But they're also talking abou IoT applications and cross-platform apps which implies an extraordinarily broad definition of UA. DOn't know that there's enough commonality to have a useful outcome. Would like to discuss where the liens are and what the dfn would look like.

Lola: part of this breakout will also talka bout the UA document. Already some stuff in that doc that kind of contradicts some of the goals of this group. GOod to think about them in tandem. The two could influence each other.

Dan: I don't like to be the person who says we already tried this and it didn't work xyz years ago... one of the early groups I cochaired was the [mobile web best practices](https://www.w3.org/TR/mobile-bp/) wg and that created a subset of html features which we said if you use only these features your application will work well on mobile browsers. Pre-iPhone. It worked for a point in time but quickly got out of date and became obsolete. Think it would be better not to do that again.

Jeffrey: on a different topic.. about UA Finding. One thing that came up was superapps considered UAs. The UA finding currently excludes them because they don't target the open web. WE should do something about that.

Lola: we have spent a lot of time talking about the high perf group. For the UA finding we want directionality for that doc. Any thoughts or ideas about that?

Marcos: prioritisation... we may not need to spend so much time on this stuff. Shut some of these things down and move on. The things we've tried before that aren't a good idea.

Lola: good to get understanding of the things that didn't work before, for those of us who weren't there

Hadley: on UA finding, a number of audience. When we first wrote EWP the logic was we keep using these concepts in our design reviews but we don't have anythign to point to to say this isn't just us on a whim, this is fundamental to the web. It was originally for our own purposes. That would be the first use I would think of for the UA finding. THen might also be helpful to thinka bout ggropus like the high perf baseline group to have those kinds of resources like our finding on UAs to refer to and help guide their thinking.

Xioacheng: the fundamental question I'd like to discuss is not about whether subsetting the web features is a good approach but how should we help diversify the user agents.

Dan: wheelhouse of the UA finding

Matthew: Taskforce for UAs? People who represent different UAs could be brought into it?

Sarven: there is an [open PR](https://github.com/w3ctag/user-agents/pull/11) that attempts to add commandline tools or web crawlers to other forms of user agents. Whether that should be part of the definition or not.. this is one example. What really can be qualified as a web user agent? Once we clarify that that also answers the slide Lola had about diversifying web user agents. Then you can understand whether the subset of that is still compatible with current web. Clarifying defintion of what a web UA is today needs to happen first. Then we can decide if the high perf user agents is going to be compatible or not.

Hadley: We have a finding against subsetting the web: https://www.w3.org/2001/tag/doc/evergreen-web/ - HBBTV wanted to take a subset of html and optimise it for TVs so they can ship the browser and the subset they could recognise at the time of making the TV and never touch it again, for 10 or 15 years. We tried to articulate why this was a problem. Subsetting slows evolution on the web overall and essentially can fork the web in a way that is really unhelpful. Browsers on exercise bicycles .. wanted to make the statement continued evolution is a good thing

Amy: We have also talked about increasing complexity of the web platform and slowing down as we're leaving older devices behind. 

Peter: the intent was that if you're building a browser into something then you should build it in such a way that it can be updated.

Yves: security is also helping in that front... if your browser is too old then the key technologies won't be supported.

Xiaocheng: clarify that the goal of the subset is not to define a subset and stop there but rather for these UA implementations to start with.

Amy: minimum viable UA?

Yves: CSS is publishing a baseline...

Jeffrey: if the question is what should a new user agent do first then we should get Servo and Ladybird to tell us. That doesn't subset the web because they're not done. They aren't pitching to developers saying "please target this subset".

Lola: we have people in W3C who are contributing to ladybird...

## Session 12. Breakouts

### Explainer Explainer; Adoption into WGs

#### Explainer Explainer

Present: Peter, Matthew, Dan, Amy (for first half)

Matthew: keeping friction about writing explainers low. Shouldn't keep template fixed as long as explainer contains information  we need.

Dan: what about being a note?

Amy: increases standing as part of the process

Peter: agree, sends that message

Amy: it's an internal w3c thing so it makes sense

Dan: make sure we don't raise the bar any further for making explainers more difficult to produce. We should make sure we don't imply explainers themselves must be notes

Matthew: we already struggle to get people to write the we don't want to make it harder

Amy: for someone who is fairly new - writing an explainer in a CG.. would it be more intimidating...?

Dan: i hear w3c documents themselves are not very user friendly.. frontmatter

Amy: we don't need all of that do we? 

Peter: we can strip boilerplate or put it behind a closed `details`. WE've talked in the past.. lifecycel of exlpainers.. over time and as the spec matures more of the explainer move into the spec

Amy: a lot of group publish primers as notes

Peter: the good parts

Matthew: agree some could be in the spec if the spec is mature, but you wouldn't expect to find alternatives considered there

Peter: useful for specs that are v1 or expected to be extended in future. Good information for the people coming next

Matthew: do you think that we should include a section for what's the roadmap? All of this stuff is 'if applicable'

Dan: that's another piece of feedback we've got generally, that they look at the template and it seems like a lot. We need to make it clear it's an informal document, relatively easy to write. It might not be easy to think about if your'e not already thinkinga bout things w'ere asking you about like user needs

Amy: maybe a formatting solution to make the template help if you're stuck on a blank page, but not imply there's a ton of mandatory stuff to fill out

Dan: do we have a separate repo for explainer explainer?

Matthew: there's a repo but the issues are in process

Dan: we should move everything there regardless of whether it's a note. [will move issues]

Amy: can we make supplementary documentation in a different format, like a short video?

Matthew: Explainer explainer explained in 2 minutes. I'd be up for that.

Lifecycle issue: https://github.com/w3ctag/tag.w3.org/issues/72

Matthew: things could move to the spec. Explainer is a lightweight living doc, should have a history that is on.... do we mandate that they're on github? THere is a history to look at earlier versions. If it's in a place where you go to the history I have no problem with sections being linked out to the spec as it gets finalised. Eventually maybe all you've got left is laternatives considered or roadmap. but it's a living doc that needs to be in sync with the spec. Whilst both are indevelopment both should be in development, as things get finalised it can move to the spec..

Amy: depends on the spec.. parts of the spec aren't necessarily serving the need and the audience the exlpainer was serving

Matthew: agree. but it's not always peoples job to write the explaier and it gets out of sync. What can we do to fix that? Is it to change the process to say if you have an explainer, when the spec goes to transition now is the time to review it

***ACTION: Matthew to add comment to existing issue to suggest this.***

Amy: definitely. Also is explainer to primer a path it can take? But not the only one.

Matthew: *tangent about the film Primer*

Matthew: So an explainer would come before a Primer (which tends to be in TR space).

Amy: Yep.

Dan: not just about primers. IN the same breath we shold be saying here are the things your explainer could evolve into and why you should make it as good as it can be. Can become material on which you build a primer, a tutorial, part of the spec, the documentation page for developers, and an important historical artefact

Matthew: flowchart for possible different states.

Dan: we can expand sentiment about explaienr turning into author-facing documentation. Important to include point about historical artefact.

***ACTION: Matthew to ake a flow chart.***

#### Adoption into WGs

Matthew: what I meant by "not w3c work" was "it doesn't have horizontal review" - added a comment in the slides to mention that.

Dan: even that... say there's someone in the community writing a spec, or they work for a browser, and want to add toast to the web. We want to make sure CGs seem to be a welcoming departure lounge into the greater world of web standards

Matthew: the challenge is those are the people who have been tasked to work on the stuff and we need to welcome them and make sure their input is got. AND (but) the decision they're going to ship this before it's had HRis the problem

Dan: yes, and I don't think we as the TAG can tell people when they should and shouldn't ship things

Matthew: agree..

Dan: we need to make it clearer that if you put something in a CG that is not the end of the story. By doing that you are committing to working on it through the w3c process including horizontal review and getting it into a charter. If you ship something you need to make sure you have a trajectory for that thing that includes the full w3c process.

Matthew: we're not chartered to review CG stuff, especially not above the other stuff we're doing. WE'd love to make it so CGs are vigorously encouraged to tell a HR group they are starting something so we can be there from the start and have better impact early on. But it's not in our scope. I don't want to be operating in that area. It needs to be udnerstood this is how the world i and we need to work with it.

Dan: we could encourage the hr groups themselves to accommdoate work as needed from community groups, to include CGs into their charters in some way, as far as possible, when CGs request their help. SEcondly we in the TAG one of the rasons the design review process is helpful is because it is often the first kind of wide review that spec authors are getting. It's tat that point we can give them a taster session of wide review. This is why we say to read the design principles, privacy principles, accessibility questionnaire... Those things are all hlep to set the mindset.. and then allow us to set tracking issues on those things so those other groups can gain awareness of them. That is one way we can help.

Matthew: we need to make that something impressed on community groups - to contact HR groups when they start working on a document... We've tried to look at whats going on in CG groups and we haven't had the bandwidth.

Dan: so in effect when something comes through the Blink/Chromium process (which does cause us to receive a lot of issues) the positive aspet is that we can signal to horizontal groups that something needs to be looked at. We could do more of this through the triage process. We can play a bridging role there. So then it's not on the CG to reach out to the horizontal group, which may be daunting. But they have been told how to make a TAG proposal.

Matthew: A positive example of this recently was the CSS issues we have had recently - there is a big picture that became apparent thanks to my involvement in TAG and benfiting from TAG members' experience to know what the wider issue is.

Dan: So we need to think about what we do as TAG, and what can be done to improve the hori\ontal review process. Matthew you are best placed to contribute to the horizontal review process part.

Matthew: Also there's the AB's considerations  - AB is looking at this to some degree. Other piece of this from w3c - one of the new AB members - elena? - Expressed a desire to make spinning up working groups more light weight, more nimble. That might address some of the concerns Chromium have raised about moving things from a CG to a wg.  From a TAG poV we can includin in our process... it could be as easy as attaching the label i18n-tracker, a11y-tracker, privacy-tracker. 

*All wondering if that might be too much info, too fast.*]

Peter: it should be a positive signal that they should look at it.

Dan: Agree, we need to exercise some discretion.

Matthew: for css ones - if a11y-tracker had been put on the parent issue then that would have helped [APA].

Dan: Outcomes

Matthew: TAG should make part of the triage process giving a heads-up to other HR groups... Adding the labels. I can email the HR groups giving them a heads up 

Dan: we need to be intentional about it. Signalling each HR group.

Matthew: cam we also encourage CGs to contact Horizonal Review groups when they start acting on documents... 

Dan: friction of making a formal request vs. individual issues

Matthew: constantly reviewing others' issues ... out of charter... requires a change to w3c process.... 3rd thing: notifcation should be a very low friction. E.g. a template in each HR group's review repo that says "I'm a CG. I just wanted to let you know we're working on this."

Dan: (1) should we do this automatically when a review request happens and (2) should these requests also use the same explainer explainer...

Matthew: Huge +1 to point 2.

Matthew: APA can make such a template. The missing piece is getting that info to CGs. We can go through Dom or others... We [APA] can tell other HR groups ...

Matthew: a lot of CGs set up by people working in companies .. that might not have expertise in A11y or other HR functions... we could use this to help recruit people to help with the HR groups as well.

Matthew: Another action on me : report back soon to the TAG about what the AB is proposing.

##### Summary

* Proposed TAG triage process tweaks
* Matthew to report back on AB work
* APA to offer a low-friction way for CGs to notify of explainers for new work.
* Matthew to complete investigation into HR short and long questionnaires and ensure the accessibility one is in the TAG process. (Think it may already be in APA's - also want to ensure parity with where the answers get filed with other HR groups.)
* (others as noted above :-))

### User agents and high performance baseline

Lola: Start with the UA finding. Second half on high-performance baseline.

Lola: I noted Marcos mentioned prioritization of the whole conversation. Hadley mentioned that the document is for a number of audiences. Serves as a justification of the TAG's design review decisions. Also a resource for groups working on things affecting UAs. 

Jeffrey: I suggest we go through the [issues](https://github.com/w3ctag/user-agents/issues/) and create opinions on each one.

#### [Clarify the scope or definition of what constitutes web user agent #14](https://github.com/w3ctag/user-agents/issues/14)

Sarven: Add web crawlers and command line things? We also discussed this earlier in the meeting so the question is what really qualifies. Figured we need to resolve that issue before answering other questions or making changes.

Yves: And Assistive Technology?

Jeffrey: Browser is the common UA because the user interacts with it. The definition includes that combination but maybe we should say more implicitly. I'm pretty sure we shuldn't count web crawlers as UAs beacuse thye are used for different purposes and not always using individuals or deal with a webpage. There are components of systems, like LLMs as user agents and they use crawlers internally but ??? issue 12 talks about this as well. My sense is that the library that helps a UA but in themselves they're not.

Xiaocheng: WebView: I agree that a WebView isn't a UA, but bringing up MiniApp platforms. 

Jeffrey: I agree that the Super Apps are UAs. We could broaden to talk about super apps and OS but then we are not talking as much about.. whereas superapps can't browse general websites (I think)

Lola: Another question for Xiaocheng: are there circumstances where SuperApps interact with the open web? 

Xiaocheng: What do you mean by the open web? Super apps can't access arbitrary websites. That also excludes RSS, email. Super Apps can only access installed miniapps. But installed ones are skeletons of the apps, and the actual content is obtained from the web. The way you present the content is using web technology.

Lola: RSS readers: engage with web content on behalf of a user. If superapps can engage with web content on behalf of the user, that matches the definition in the finding. Current definition doesn't mention the open web.

Xiaocheng: Tricky: super apps don't interact with websites. But with web content.

Jeffrey: i feel RSS and email readers are UAs but we shouldn't be talking baout in this finding. Just being built with web tech not make it a website. I don't want ot imply that my thought should define what we do but that's where I'm leaving..

Xiaocheng: Narrow scope to web user agents?

Jeffrey: We already had a scope of web user agents, but what does that mean?

Lola: RSS readers?

Jeffrey: If they only read the RSS format, they're not really web user agents. If they include a webview, then they do become a web user agent.

Sarven: Interestingly, for example, Wikipedia entry https://en.wikipedia.org/wiki/User_agent (perhaps common use) and MDN entry user agent https://developer.mozilla.org/en-US/docs/Glossary/User_agent considers even "bot scraping webpages, a download manager, or another app accessing the Web." That said, my general view is very much a user-driven agent acting on behalf of the user interacting with the web.

Yves: Depends on the angle. HTTP spec, a UA is something that does an HTTP request and gets a response. But here we're tlaking about things that act on behalf of a user, which is different from things that act on the network level.

Lola: Document is called "User Agents". Add "Web"?

Jeffrey: There's a PR. I was skeptical, and I'm not anymore. Merge that?

Lola: Sarven's PR 11?

Sarven: Don't mind the conflict with MDN/Wikipedia. Feeling is that we want to talk about user-driven software. However the user interacts with the agent, e.g. voice, telepathy...

Yves: With an LLM, it only interacts with the web during training. When it reads a picture, then it's interacting on behalf of a user.

Sarven: Are there intermediaries? Whether the UA has a close communication channel, or there are intermediaries? E.g. with an LLM, it looks it up and queries the web for you. So LLMs that can do that would qualify as a UA or at least have the UA capability.

#### [State the intended audience of the document #13](https://github.com/w3ctag/user-agents/issues/13)

#### High Performance Baseline

Lola: Discussion in the big group was very opinionated. Xiaocheng, what do you want to get from us?

Xiaocheng: Big questions:
* Do we want to help diversify user agents?
* Do we think defining a subset of web features is a viable path toward diversifying user agents?
* If yes, what are the concerns and how do we tackle them? If no, are there other viable paths?

Do we want to help diversify user agents?

Xiaocheng: Yes.

Jeffrey: I agree.

Lola: How are you thinking about that?

Xiaocheng: Right now, user agents, and especially browser engines, there are only 3. Significant amount of browsers are Chromium-based. Would be good if there were somethign new.

Lola: For this discussion, are we mainly talking about browsers?

Xiaocheng: No.

Lola: Miniapp platforms. What else?

Xiaocheng: that's the whole list for now.

Jeffrey: yes it is very important that we get more browser agents. we have serve and ladybird working on / part way done. i think it'd be important to get one successful one than three partial ones. i dont know how the tag can help concretely to make that happen. whether a subset is a viable path to diversify user agents. For that, my instinct is no. Picking a subset would only help if big chunk of websites implement that subset and than we still have the problem the UA took that and can browser the subset and that seems like a problem. Evergreenweb ... as evidence that this hasn't been a good idea in the past but doesn't prove that is not a good idea now.

Lola: A lot has changed in that time. Is the landscape ready to do the exploration again.

Jeffrey: I want to be open to that possibility. Probably not but maybe.. 

Lola: Learning from Evergreen

Jeffrey: The consideration may be that why would devs develop to that subset and part of the answer may be that they get access to the miniapps platform. maybe easier to install if developed to that subset. that can happen if incentivised.

Xiaocheng: Clarification: probably not good to start with the subset.

Jeffrey: which means it is not a long term way of making UA development easier. It just helps one round of engines now.

Xiaochang: It lowers the threshold

Jeffrey: I don't see that. In order to help it we need devs to adopt the subset. But the next round of engines don't benefit it. if we get two new engines out of this that's a benefit out of htis.

Xiaocheng: Although I also have some doubt on this answer: The set of features is highly ??? very frequently used subset among those ??? . Tencent defined a DSL which is a subset.

Jeffrey: For the CG, instead of advocatin ing the devs to take the subset, 

Xiaocheng: We discussed short/long term but don't have a clear idea.

Jeffrey: servo/ladybird aren't involved wtih the cg?

Xiaocheng: Ladybird is not. there's collaboration with Igalia but need to check the reference.

Jeffrey: maybe we should discuss this as advice to UA devs in what order they should approach the features. 

Yves: baseline as priorities rather than subsetting

Xiaocheng: any advice to talk to the cg? ill summarise the discussion and give it to the cg

Lola: the CG needs to consider changing the name.

Jeffrey: "Recommended Feature Prioritisation for Developers of new Browser Engines"

Xiaocheng: Interoperability: Encouraging incomplete implementations.

Jeffrey: as long the plan is to finish the implementation it may be fine. don't advertise until finished. we cant force a browser engine to be finished before people use it. the incomplete state is acceptable.

Sarven: Concerned that it's not just a subset but actually a fork that won't be compatible with existing UAs. 

Jeffrey: That there are sites that'll work with these new engines but not the old engines?

Sarven: Maybe. Vendor might create 2 sites. Separate representations of how they express their own information. I think that's a major concern.

Xiaocheng: Whether we're forking the web is discussed in teh CG. CG says no. Any feature in the subset needs to be a web-compatible feature. If a site targets this subset, it'll work in existing engines. Vendors creating 2 sites: that's already the reality

Sarven: Will the same representation from https://example.org/ be used by both traditional web browser and the miniapps? otherwise, the server wouldn't be able to tell what representation to serve who without conneg (different mediatype) or checking UA header. Which is not great.

Jeffrey: Progressive enhancement using the many existing techniques.

Sarven: is that what the CG is doing?

Xiaocheng: that wasn't discussed in the CG.

Jeffrey: Anything else?

Xiaocheng: When defining a subset, we need to use a certain granularity of features, and that should align with WebDX?

Lola: Yes.

Jeffrey: I'd say that when naming features, you should use the names that WebDX picked.

Lola: They have a [repository with feature names](https://github.com/web-platform-dx/web-features).

Xiaocheng: From our experience with developing a new engine, "what is a feature" is a difficult problem.

Jeffrey: Hopefully, if you copy WebDX, you won't have to re-solve that problem.

Xiaocheng: Alternative approaches to help new UA developers?

Jeffrey: Join existing small engine, like Servo or Ladybird. 

Xiaocheng: Risks creating just another Chromium-based browser. If you want a new engine that just works, maybe just use Chromium. New developers are much smaller groups than the Chromium community. A new developer's repository might just be downstream of Chromium.

Jeffrey: The company funding the new engine should have a really clear business case for doing so. It's good for the Web to get a full new engine, but most companies will be better off doing a Chromium-based browser. The business case will determine whether they can contribute to an existing new engine (more likely to succeed) or if they need to start an entirely new one (less likely).



### AI

DanHadley we could add energy to the ethical AI principles. Work out if it's worth our while to take on the doc, help it evolve. 

How it impacts the sustainability (as Tristan mentioned yesterday)

Martin: presently unsustainable

Hadley: also financially unsustainable 

Dan: from the document Dom wrote, which one makes sense to impact what other people are doing. Maybe start with the proposals from Chrome?

Focused and balanced: not too much AI sucks and not too much AI is awesome

Hadley: It also should be actionable.

AI and the web (Dominique Hazael-Massieux) https://www.w3.org/reports/ai-web-impact/ 

Martin: we could make a brief statement to say "AI should be ethical, accountable, etc"

Martin: the IETF are working on providing a consent model for labelling content. 

Martin: there are two approaches to this. You might want to label genuine content, and you might want to label AI content. 

Hadley: when people are trying to deceive, they would not add a watermark. 

Martin: there’s a case that mathematic is impossible. Because you can keep tweaking the image to make it not detectable by the system that confirms if it’s AI.

Martin: What is the best place to have discussions and speak with authority. 

Martin: I don’t know why an API is using some ML model would be useful, but the Web Apps might not pass that on or why the user might care.

Martin: the data stuff might not be very applicable. 

Hadley: that’s not the use case that he has in mind. About impersonation.

Martin: if someone creates a deep fake about you, and it’s someone that you trust, it probably won’t help. 

Hadley: having an identity system might help if the person can prove they are a person

Martin: talks about sustainability. Which the sustainability work could cover to a degree. 

Martin: interoperability…

Hadley: interoperability or models or results? 

Martin: how do you deal with the non-determinism. That needs to left to the model creator.

Hadley: so you can define standards for the way in and for the way out. There are other APIS where there is also a box that obscures what happens inside. 

Martin: so, that’s that list.

Hadley: so why does it have to be the TAG? 

Martin: there might not be anything specific to the Web. 

Martin: Right, but we are not a sociologists, ethicist. Maybe the Ethical web is enough? 

Hadley: Yes, that might be sufficient. 

Martin: there are better things that could be said by other organizations that are better placed to make such statements. 

Martin: The fundamental problems is that these principles may be self serving when written by a particular group. 

Martin: the neutrality of the model can be question. 

Hadley: right, but then if the AI is serving as a user agent, then it could fall under the User Agent work. 

Tristan: Open AI has talked about putting advertisement into their model

Martin: the output can be biased and it’s not transparent how the results are in. 

Hadley: here are 4-5 specific points to think about that need 

AI is becoming user agents
AI generated content is becoming more available on the web, posing a challenges for search engines
Content is at risk.
Tristan: AI can be useful for instance for alt= text. 

Martin: yes, Mozilla has built such a tool 

Martin: ML based translation is very useful. 

Tristan: from an sustainability perspective, there tools require a lot of computation or specialized hardware.  The thing about the web is that it is low tech. Companies are looking to use AI to sell more devices. 

Martin: which may encourage people to buy more devices. 

Marcos: there is specialized hardware to do AI efficiency. 

Tristan: there is a lot of environment cost in the development of the devices, their transport.

MC: I challenge that the web is low tech, as they still fully utilize all available hardware. 

Tristan: With respect to morse law and the ability of computing power, developer can become careless with the use of computational resources. 

MC: browser engines compete on speed and power efficiency. But yes, computing resources could be ineffectively utilized

Tristan: there’s examples of people how people can solve problems very inefficiently.   

MC: there’s responsibility on web Authors to produce high quality. 

Hadley: I’m worried about where the models are run, and how much they cache, and which box they run in

Martin: yes, this is also a user agent problem across boxes and context. How much personalization should there be and by who. 

Hadley: what could the TAG finding say? 

Marcos: we should look at the API proposal from Google and maybe something the TAG should say should come out of that. 

Hadley: that seems reasonable. 


## Planning

(plenary)

### Meeting schedule

https://tag-github-bot.w3.org/util/scheduling

### weekly call times

Keep the current breakouts until 1 April. 

Breakouts (April through October approximately, pin to UTC, revise ahead of the October transition):
* Tuesday 11:00 China time / 13:00 AEST / 20:00 US-Pacific / 03:00 UTC
* Wednesday 17:00 UTC / 18:00 London (BST) / 19:00 Paris (CEST) / 10:00 US-Pacific
* Thursday 09:00 UTC / 10:00 London (BST) / 11:00 Paris (CEST) / 17:00 China / 20:00 AEST

Plenaries, one meeting per fortnight, alternating between two times:
* Wednesday 08:00 Paris (CEST); 16:00 AEST; 14:00 China; 07:00 London; 23:00 US-Pacific (6:00 UTC)
* Thursday 23:00 Sydney; 21:00 China; 15:00 Paris (CEST); 14:00 London ; 6:00 US-Pacific



Matthew: for each call we should know what time zone it's pegged to

Sarven: I answered my based on current daylightsavings not the future

**We agree to schedule a f2f in early September 2025 (location tbd but we discussed somewhere in Asia). We also agreed to do something like a virtual or hybrid f2f in June time-frame. Dan to come up with a new format.**



*we agree should set our meetings to be 55 minutes*

### f2f meetings

Martin: I propose we meet once more again - maybe in September - and then meet (briefly) at TPAC.

Early in Sept, to keep distance from TPAC.

Dan: propose we meet f2f in Sept. Between now and then, a virtual f2f but not what the previous format. Less taxing, perhaps hybrid? Perhaps in June.


## TPAC - what should we do? 

Martin: TPAC is in November - 10-14 - late in the year. We don't have time for a f2f after that...  Was going to look 

proposes 1 more f2f. 



## Upcoming AC meeting in April - who is attending? 

Xiaocheng, Matthew, maybe Tristan.

To join our TAG presentation to the AC, be there to answer questions. 

Join a session on human rights? 

## Architecture & Commons Discussion - we agreed we would talk about actions.

IASC: https://iasc-commons.org/

Conference 2025: https://2025.iasc-commons.org/

Jeffrey: should we go to the commons meeting in June in Amherst. This is our opportunity to participate in the academic community.

Lola: I would like to say yes, but what have previous interactions been?

Jeffrey: my theory is that there could be a PhD student who could get a PhD out of this... but no candidate yet. We've talked to a couple of academics .. who have said here are things to look into. I feel like we're not the group to go into detail... on how the web acts as a commons. We want to produce guidance based on that lens but not be the ones to do the research.

Hadley: also for discussion - we had talked in the opening session about actions.

Jeffrey: so: do we publish a doc saying "this is how we think the web acts as a commons" or do we hold that until we have practical implications for design principles, or somewhere in between. 

Hadley: I think it would be helpful to talks about the other parts of the web's architecture... e.g. search engines, mobile apps, ads ecosystem... 

Jeffrey: we could step back and say "here is the emergent architecture" and have a section of that that mentions the commons lens. Architecture as the primary deliverable.

Matthew: I like the idea of describing it as it is. if we come back later and make principles then we have something to cite. It seems like what you're talking about - something in between - the challenge is that the commmons wording could cause confusion to those who read w3c stuff... sensitive to that. Should be accessible to our audience. Like the idea of modeling the web - all the different actors.

Jeffrey: I'm hearing that we should start a document on the emergent architecture - mention the commons lens there but not focus on it... 

Matthew: the doc you have now - sets out the actors, "resources" (noting this is a part that needs re-framing), and motivations... wouldn't want to lose that 1:1 mapping to the Commons work/world...

Dan: I don't want to block this... I think it would be great to do this and publish and updated design principles that includes a link to this. To demonstrate the link and produce more actionable guidance. 

Sarven: this is compatible with what i thought as webarch vol 2... there's a lot more technical aspects ... all of this would go into this type of document. 

Jeffrey: i feel good about this. Seems like right direction.

Sarven: This is a document we would like to start writing.  Who would like to work on this?

Jeffrey: I will start a document in google doc.

Sarven: I would also like to edit.

**break**

## Retrospective

Amy: There are a couple of questions I have for the room before we get started. Want to start with a round of check-ins to ground everyone in the now. How are you feeling following this week?

*round of check-ins*

Amy: The other question I had, which I think has been answered by these rounds was whether we should focus on the f2f, or the last quarter, and I'm hearing both, so will try to focus on both.

Rounds: everyone will be given the opportunity to speak on a particular question. Make one point each round. If you have more than one thing, we will do multiple rounds. If you don't have anything to add, you can skip a round.

If someone says something you were going to say, you can agree with it and say something else, or you can move on.

We are not responding directly to things that others have said - we are recording this, so we can come back to the points later. We are solution-focused people so I'll try to introduce some forward-looking stuff.

Dan: Can we ask clarifying questions?

Amy: Yes, but got to keep to just that. Time and equity of contributions are important.

We are going to do a rounds to gather the topics that we'll talk about. Whether that's related to the last 3 days, or recent experiences with the TAG in general. I will look at these and pick out the focuses/themes, and pick 3 or 4 topics on which we will have rounds.

### Topics rounds

* f2f
  - How we decide on agendas
  - How we use the time (big picture vs closing issues)
* the past quarter
  - Ways of working (including betwee calls, PRs, ...)
  - Technical leadership - agneda-setting; longer-term TAG work
* stretch goal: chairing
* If appetite for discussing things like councils, we could run into the next session

Martin: We must discuss associates as part of ways of working.

Amy: rounds on topics; the first is what went well; second is what didn't go well (try not to solutionize!); then a round on next steps (keep it short; we don't need to work out the details).

### How we use the time at the f2f meetings

About high-bandwidth discussions on big topics. and the work of doing design reviews, priniples, hands-on stuff.

#### What's been going well?

* THe way we chose topics and allocated time with introduction, breakout, and retro on each topic was a very good use of our time. The topics picked were by and large important, pressing topics. Happy with that allocation.
* It was good that we focused on the big topiocs and talked in a high-bandwidth setting about what to do in general.
* It was good that everybody here felt very switched-on and present during this meeting.
* It was a good sign that mulitple times I heard people want to be in multiple sessions.
* The way we structured it made it engaging.
* Yes and we came up with deliverables.
* We are continuing to experiment with the balance betwee plenary sessions and breakouts, and how those two mix.
* The three-session format allowed me to advance my own thinking through discusson on a number of topics.
* The length of the sessions was not too short, nor to long.

#### Things that could be improved

* I see a tendancy to shift from a conersatonal style to a queue-oriented style; important to maintain a balance there.
* Maybe to do with how we arranged the agendas, but should've arranged it so we could've closed more things in the breakouts.
* For the breakouts, we didn't need to dive into the inner details of issues. Sometimes we found ourselves trying to process the issue from scratch. The group could've used the time better for high-bandwidth things. Being on your feet and trying to address bigger things.
* We put too much time into the reporting back sessions. Could've shortened them if we'd planned in advance.
* The days are too long. I would be happy with 4 days, but shorter days.
* We should commit to what we are going to do. We didn't prioritise design reviews in the planning.
* I was not as prepared as I could've been - will endeavour to do more on this next time.
* Lack of social activities.
* Lack of 1:1 time to close things with specific people. Less discussion; more pair programming/writing. I value and need this time to pump out as much TAG stuff as possible when here.
* Picking and arranging the topics for the sessions was very difficult.
* The level of prep requried for participating in a session was unclear - wasn't obvious how much we needed to know about the topics going in. Different sessions for topics were run differently in this respect.
* Knowing the topics in advance before the f2f could help. A fixed set of topics people can prepare for.
* Not enough notice on prep activities.
* More laptops down time. Wasn't sure how much to prepare for slides / expectations on that.

#### Next steps micro-round / summary

* On topic of getting more time in f2f or virtual sessions to do 1:1 pair work, which was successful from [capital of iceland] meeting, we need to get back to do that, but we need a better tool.
* Some people are going to put forward proposals for how we better use our time - balance (including work-life balance); ...
* Next time: advance prep: a week before. (Chairs to instigate this - make it clear what the rest of TAG needs to prep)

### Agendas for the f2f meetings

How do we decide what to work on at a f2f?

### Technical leadership

Focus on TAG's leadership within W3C, how we determine on what we'll work, considering what comes up, what's OBE, focusing on high-level community involvement.

#### What went well

* THe discussions we had this meeting about documenting the architecutrue and taking charge of incubation seem to be going in the right direction.
* When mentioning a dcoument TAG is working on on AB member-lead meetings, there is always really positive feedback from Team and other W3C members. A good example is Societal Impacts queestionnaire. Feedback like "that's what we need". Feels like we are doing something good on technical leadership here.
* We're listening to what's going on in the world and bringing it to the TAG.
* It's been helpful to reach for TAG Findings and other docs, as a spec editor. Gives back up, especially for when deadling with orgs outside of W3C.
* Publication of Statments. Means it's not only the voice of the TAG but of W3C as well.
* TAG's commitment to not be a secret cabal, and have a wider relationship with the development community.
* We've got to the point where a lot of the TAG design review is self-service; people can look at desgin principles and find a comprehensive set of advice to help them steer away from rocks in congested waters.
* Quite often, people do listen when TAG says something.
* Giving guidance to groups (people using specs, ...) as this is technical leadership.
* W3C CEO asking for TAG feedback and guidance that showed up in presentation at TPAC and something that has been sought since for board and strategy meetings.

#### What could be improved?

* Incubation - a lot of responsibility lies with the Team. I am not 100% happy with that situation.
* More developer meet-ups please!
* We struggle with our written work, both trying to get things out in a timely manner in order to make an impact on a particular issue/decision, and also trying to make them thorough and well-reviewed.
* More engagement with regulators, or creating documents targeted towards regulators. There are a lot of problems the web and the world is faccing that need more than a tech. solution
* Communication with wider community. E.g. we are haphazzard about how we use social media.
* Be more crystal clear on whether a group or author should submit an explainer. Checks on that process. It'll save them time. Make sure it's clear to them that that's something early in the process.
* W3C doesn't charter quite the right work, and we don't have an idea of what that is - seems like our responsibility but not sure how to fill it.
* We could be doing more to cross-collaborate with other standards bodies, people doing simlar things on the web.
* We focus on technical leadership but other topics about the f2f, planning. Would it be better to prioritise each quarter?
* Re not knowing what should be chartered... occasionally we do, but we don't have a way of making it happen.
* Folks proposing explainers shouldn't review them.
* We don't have a good idea of which features we should be reviewing. We are haphazard about which we pick up, and get mad about some.

#### Next steps

* Have smaller developer or TAG events in whatever hub we are in.
* We have a document about how you speak as a member of an elected body - important to remind yourselves of that.
* Several ideas came about incubation and HR, which work at TAG and other levels, will recap in the later session.
* High-level topic prioritizing on the agenda for the next f2f.
* Team has funnel; that seems to be the place setting the priorities. Other priorities should come from the membership. A lot of us chair groups and know the priorities. Could talk to the chairs more. Have a set of priorities for the year that are high-impact and need attention. Areas that need a push. Take input from members and groups.
* Could find time for a quick chat about how we communicate. I used to put out on social media a summary of breakouts or f2f sessions. Then we started splitting into breakouts that were parallel so I felt I was missing what was going on. Then my attention was too split. Now we are planning to focus more on a smaller gorup of topics we could revisit this.
* Guidance about people in elected groups - we should be reviewing that, but not be afraid to use our individual voices to engage and show technical leadership _in a constructive way_. One constructive thing we could all do is after this meeting and we go home, if we all 'blog about this meeting.
* Set agendas in a more co-ordinated way, by doing things like adding agenda+ to issues. Milestone-based scheduling not working well.
* Design reviews: lean on associates more.
* Chartering: more willing to charter stuff to bring it in under the umbrella of W3C.


#### How we get stuff done

##### What went well

* 1-1 chat with an Associate. Gave a backgrounder. Felt it can go smoothly.
* Have experience with working with community people
* Seen we're good at closing design reviews. It has improved in the sense that people come to meetings. We're not idling on the calls.
* We know mor or less know our interests. That lead to knowing who is looking at issues, and who is ready to continue on somehting, and lean on respecting people and their opinion on working things.
* The individual TAG members are wwhat's working best. The work that I do is better having others involved.
* Making progress on the calls. Taking a step forward almost every time.
* Design principles has become enormously valuable.
* With any time you need to have on things stuff done and getting to know each other and inject all sorts of stuff. We do pretty good at that.
* There has been a couple of convos where there may be tentions but it turned out great.
* As a new member, it was relatively easy to dive into things, welcoming, no push back.


##### What can improve

* Try to be better at ensuring thta the right people are there to discuss issues. Related to planning.
* Unclear on the intentions of the Associates.
* I'd like to see a shift to ask more associates to do more or something else.
* Like to see more effort on doing work prior to meetings.
* Stuff that I've spoken to about what to expect from associates, it is not written down anywhere.
* There is a lot of oral history that need sto be written down.
* How can I make my time benefit more the TAG. I join calls but feel useless and don't want to.
* Find smaller and focused tasks. Solve a thing in an hour.
* Uneven level of participation across the TAG. That's fine but it is not always right that expertise is under-utilised.
* Everyone who is on the TAG has expertise and has a reasons. We need to be more intentional on that.
* I'd like to explore more 1-1 breakpouts during our non-F2F weeks. It has been valuable to do 1-1 and if we can do more of that.
* We need to figure out ways and improve attendance on calls.
* re remote breakouts, there were changes to the calendar that were not communicated, so that was confusing.
* Pair programming, whether co-editing or tackling an issue. Quicker feedback
* Find ways to support people to attend calls.

## Reporting back from morning breakouts

*Refer to notes above - this is for brief summary, and new things.*

### AI

Martin: we went through Dom’s document
Martin: and what we could say on the subject.
Martin: we could add much that the TAG could add to, because either to document covers it or it’s not in the TAG’s scope
Martin: so we look at what we might be able to add to the discussions
Martin: we discussed the Google API and we gave ChatGPT to produce a critique. 
Martin: In terms of things the TAG can say, we have a bunch of principles by which we judge web features and that AI is not really special in that respect. We can just point to the existing TAG’s work. 
Martin: we can make it short and punchy and just refer to the things we.
Martin: we judge them by the set of criteria - is this good for AI. 
Dan: who is going to be the editor or that finding?
Martin: we haven’t had the discussion with the chair
Martin: I would be able to pump something out pretty quickly, but I’m committed to do the digital credentials stuff. 
Jeffrey: ok, and you can check with Hadley async.
Dan: I think it’s a good start. 


### User Agents and High performance baseline

Lola: first thing is that we addressed some syntax and language stuff around UA finding document. Making sure we separate what happens when you visit a web page vs. a user giving consent for a web page to do things...  The proposed change to the language includes an insinuation that something should happen when you visit a web page 

Jeffrey: review of #PR9... Sarven re-arranged the language... the current thing says "when you just visit, nothing happens then users can make stuff happen"... We will continue to iterate. 

Lola: we also spoke about High Performance Baseline CG - we suggested they change their name. We decided that Miniapp platforms are not "web user agents" and UA finding should probably not talk about them.  Also talk "UA" doc title to "Web User Agents".  

Lola: we recommended that the group speak to new browsers such as ladybird & servo about what they deem is important - use that to inform a subset. However on the subset thing - taking into account Dan's and Hadley's points, has the landscape changed enough so this might work now? 

Jeffrey: we also clarified that Xiaocheng's impression of what the CG wants to do : give advice to implementers wanting to build new browser engines... 

Martin: [what about just implement Baseline]

Jeffrey: the question they are trying to answer is - what's the smallest set of features that allows the most web sites to work?

Jeffrey: another piece of advice: anyone thinking about implementing a new browser engine should make sure they have a really good business case for it. 

### Explainer Explainer; Adoption into WGs

Matthew: We do think it's a good idea to make it a Note - not a barrier to those wanting to write explainers.  We've got some neat ideas to make it more accessibile as a document... Explain more about the lifecycle of explainers... What end state of explainers, etc... e.g. primer, .. writing a flowchart... 

Dan: We also moved all the issues to the new repo.

Jeffrey: do we have consensus to auto-publish this to TR space? And it's a full Note rather than a draft note. I think it's ready to be a Note.

**CONSENSUS IS RECORDED**

Matthew: Adoption into working groups... covered a lot of ground.  I am going to attend the AB's meeting tomorrow and see what they are working on wrt incubation. APA is going to offer a low-friction way for CGs to let them know about new explainers for new work.  I am doing work on this.  

Dan: we can add notifications of HR to our triage for new things that come in for design review.

Yves: we need to inform HR groups of this...


-----

**Resolved: Thank you to Tristan for hosting.**
