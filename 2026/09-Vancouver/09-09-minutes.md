# TAG Minutes - 9 Sep 2026 - Vancouver F2F

Present: Brian, Heather, Marcos, Yves, Christian, Jeffrey, Sarven, Lola, Matthew

## Engaging with proponents as TAG vs Individuals

Lola: This question came up multiple times this year (DAS, WebMCP, …). Proponents have come to us with something, and as we’re trying to understand it, we as individuals have questions. The problem is, the proponents don’t see you as individuals, but instead as a TAG representative. We tried to solve DAS through the deputy model, but that didn’t work. For WebMCP, we had the Google Doc, and that also didn’t work. Don’t know how we can address this. Even if you’re just asking “as person A,” people will see you are “person A from big-tech company B.”

Marcos: It might be part of the strategic play of proponents to blame big-tech. I believe that the deputy process worked well, we might also ask whether the proponents thought the same. Not sure if we can change this at all. WebMCP is another case. Don’t believe my position to change depending on the company I work for.

Yves: I want to remind you of the Elected Body Communication Guidelines (https://www.w3.org/guide/other/elected-body-communication-guidelines.html), which is a great read for newcomers. By default, interactions with TAG members are on an individual level.

Heather: Similar problem comes up with Working Group chairs. Even if people say they speak as an individual, other people may not see you being able to do that. Reiterating what role you are playing when you’re responding works really well from my experience.

Marcos: All of my responses were prefixed with "as a (role)" after that case. Agree it can be potentially confusing. And if it is not, it can be weaponized.

Jeffrey: Lola, you said did you mean with "it did not work?"

Lola: With WebMCP, we provided them a document with everyone’s individual questions. The proponents engaged with the document. On the document, in big, bold letters, it read “THIS DOES NOT REFLECT TAG CONSENSUS,” but they still interpreted the contents of this document as such, when they joined the meeting. We invited them to a TAG plenary meeting to discuss the questions individuals had. Can’t remember the details of DAS. Impression I got was even with Christian as the go-between, (TAG members) continued to go around the go-between. What do you think, Christian?

Christian: I think the deputy model was successful, we were able to close the design review. It did not avoid the FO, though.

Jeffrey: Christian could have been more active. Once we said Christian was the only individual who should interact with them, it is true that Marcos continued to interact with the proponents. That should have been Christian. I intentionally stepped back. Agree we can’t rely on the defaults.

Marcos: I was assigned to speak on behalf of the WebKit team, so I had multiple roles at once to fulfill.

Brian: Think it’s important that we are able to ask questions, that must be possible.

Sarven: Maybe we should always put disclaimers there, even if it didn’t work with the big red letters. Maybe we should only voice TAG positions at certain places, and only there.

Christian: We should be careful and state what role we currently have. On the deputy model, it would have been helpful if I'd stopped Marcos from interacting? 

Jeffrey: It's a tricky balance when there are competing roles in the same person.

Marcos: Also, you were on vacation.

Lola: We are doing a retrospective now; this isn't an "at fault" conversation. 

Jeffrey: You also mentioned that in the WebMCP discussion, there was a list of questions, which the proponents treated as TAG questions. Don’t think it’s an issue if “the TAG has a question.” A concern or something would indeed be a problem. What’s the danger you’re worried about there?

Lola: The problem was that people weren’t in the actual meeting (it was only a breakout), so nobody could say if the answer was satisfactory.

Jeffrey: If we have a scenario like this and people can’t be there, the other members in the call need to understand the gist of the question.

Lola: There were a lot of questions, and some of them were quite detailed.

Marcos: We thought had pressure there. The situation was kind of unique. Also, we’ve invited five people and they showed up with 20.

Brian: Several things added to that: the artificial pressure, the lengthy document, people reached out to me directly—are these TAG questions? Even it said the disclaimer at the top. Very few times we invite somebody. Might feel you’re called before the judge. We should normalize that a little more. Maybe by having more discussions with people, and making it very clear in the invitation and the outset, that you’re not called to the principle’s office. The assumption isn’t that you’re wrong and we are going to tell you… but rather, we want to understand your background.

Christian: Retrospectively, we should have cancelled the meeting. I felt a little thrown under the bus. The reviewers with the critical feedback were not there, and I wasn’t aware of that. I couldn’t get myself to represent their position in that short time span. Also, there were 20 people on the other side.

Marcos: We need to make sure that stuff that is so criticial as WebMCP, the TAG needs to act as one unit. People should make themselves familiar with that.

Lola: In summary, the deputy model seems to at least have been more successful than the document.

Jeffrey: The document says “feedback,” not questions. And it says “we think,” so this is not really a data point for “document of questions.”

Lola: Should we continue discussing this during the next plenary?

(Group agrees.)

## Architectural Decision Record

Slides: https://docs.google.com/presentation/d/1oKEi5uteoBiOCA1i-Nxu7M_8PuASC-4TcW1vM-NHnMo/edit?slide=id.p#slide=id.p

Jeffrey: If you think something is silly and should be fixed, you must ensure that you really understand it, as you otherwise will break things. Following this, it’s not easy to change things.

… We can ask people, there is a Git history, there is explainers, which fall out of date. The idea is that when you make a decision, you should write down the pros and cons, and check that in along with the code. That’s Architectural Decision Records (ADRs). There’s also an ISO standard on formal architecture descriptions.

… There is a GitHub organization with promotes ADRs. And an online tool to generate ADRs. I added a bit to the explainer-explainer to consider using these. Adoption doesn’t look great, though.

Brian: The trouble with all these things is that they are out-of-band from the actual discussions themselves. For example, the dictionary work. It’s three years in the making already, there have been so many discussions and changes. If I really captured all of those, probably the most efficient thing was to point to all the various discussions. Then that might be 40 pages long.

Jeffrey: It would be more something like, pointing the discussions, and explain the pros and cons.

Brian: So, alternatives considered? Who has time to read it? What do we hope to get out of it?

Jeffrey: Ok, so that’s part of the question: 1) Do we want to adopt this for our work, inside or outside the TAG itself? 2) Should we more strongly encourage design reviews to use ADRs?

Matthew: A question and a thought. The question is what the scope of this is. Which granularity? Small things that we’re changing? Or the big things? I really like conventional commits, and keep the metadata at the point of change. In projects where I use them, they seem helpful. There’s probably increasing pressure in the industry to adopt something like ADRs. If we want to be software “engineers,” we should adopt engineering principles.

Jeffrey: My understanding is that you can do an ADR for any change. Worry that the big decisions are going to get mixed in the little ones. Worry they may be hard to find.

Yves: Wonder if LLMs could prepare the “what happened,” so humans can fill in the “why” for the change. To be able to do that, we need to ask people to add as many context as possible.

Heather: Are we talking about ADRs for the documents that the TAG writes or for the design reviews?

Jeffrey: That’s an open question. Most common place is spec design. As an explainer moves to a spec, the alternatives considered should move to ADRs. So we would more actively encourage adopting them.

Brian: LLMs can summarize things from the history quite nicely. Maybe there is a middle ground? Some people argue against explainers as they duplicate the spec. Don’t like explainers where you keep scrolling, and the bar barely moves. Might be good to encourage capturing these things and making sure they are linked. Good link text?

Yves: LLMs can scan history, and answer what the reviewer is asking and explain the “what happened.”

Jeffrey: In many cases, this includes the “why.”

Sarven: If more information can be gathered, that’s great! Not very optimistic. Some groups are doing this, most don’t. Proposing that might be a nice precedent. Not sure if a lot of people would jump on it.

Jeffrey: There’s a lot of documentation on ADRs itself, so we don’t have to do that. We shouldn’t push it explicitly.

Matthew: Not sure if we have unanimity on the exact how, but remember the CRA will have an impact. We’ve already got alternatives consideres. Agree we shouldn’t force people into adopting it, but can point them at the various options to satisfy the requirements we know what’s coming up.

… On the point of linking to things, this is possible, but that’s why W3C uses IRC and all those systems. Next steps?

Lola: We haven’t actually answered that question, but we need to wrap up.

Yves: It would be good if the template of the design review adds a section on alternatives considered, so it can be crawled by a tool.

Brian: We could offer this as an alternative form for alternatives considered in the explainer template.

Jeffrey: We have that, the explainer-explainer states that already.

Lola: So no task force, but who’s interested, is invited to contribute.

## XML 1.1 obsoletion https://github.com/w3ctag/obsoletion/issues/6

Brian: Issue is open for years. I think it’s safe to say yes to obsoletion. Nobody really adopted it, there is a XML 1.0 Fifth Edition, which is identical unless for a change.

Yves: 1.1 made some update for Unicode, some people acted against that, which is why 1.0 Fifth Edition was produced. Nobody implemented XML 1.1. People in the XML world say we should obsolete it. Personally, I think it will be a good decision to obsolete this, which is what I want to propose to the TAG.

Lola: Consensus that XML 1.1 should be obsoleted?

(Group agrees.)

Yves to close the issue with a recommendation and then take it to the team.

## TAG Job Description

Draft: https://docs.google.com/document/d/1yHDYLtATHgrCwMsbBz_KLqVSTpOFDtIvaGXhvwoNGN8/edit?tab=t.0

Heather: Compiled a list of working group meetings, so we can reach out to people to put themselves up for the next TAG election. Joining all of them seems impossible, so we could instead send an informal job description to the Working Group mailing lists.

(Group is reading the draft.)

Jeffrey: Feel it’s quite lengthy.

Lola: Looks like you got enough responses and comments, so we can keep discussing this async.

Heather: Will work on this!

Jeffrey: Want to record that while we can’t go to all of the groups, we can offer that to the chairs to reach out if they think it helps.

## Global Components Design Principle

Brainstorming doc: https://docs.google.com/document/d/1QTUVSsowPfeLuNq0QuxNZNU8AvhwnVVyOto6trOCn4A/edit?tab=t.0#heading=h.qnp7snf5fhs2
Draft (V2): https://docs.google.com/document/d/1UsNl1VsYXffF6-GHayAvqWoY5YK6lLrCr6QCgPuFXM8/edit?pli=1&tab=t.0#heading=h.fdjakzwcu1q

Marcos: Downloading components to a browser (e.g., AI models, …) come up more frequently. Implications for timing attacks. Not a common thing across user agents, but could be. There’s a tension between the OS/user agent where requests are handled and downloaded. It has privacy/performance implications.

Brian: The browser already has a lot of global services, even if they are not called that.

(Shares a list of services, e.g. TTS, STT, live captioning, which can happen in the cloud, locally, or hybrid: https://gist.github.com/bkardell/6ae6a134e419338a53c465a63ef0066f)

Jeffrey: There might be a distinction between browser affordances and external software. “Components” may suggest they can be downloaded independently.

Marcos: Question is developers should not know where things happen, that should remain in user’s control. Not sure why developers should have a say on that at all. Should not make the determination for the user.

Brian: TTS has voices in the way that you have fonts. You don’t know which voices are supported, and they can even change while they are speaking. On Android, if you don’t have a HQ connection, it uses the lesser quality local model, otherwise, it is using the cloud. It switched voices mid-paragraph. Not the voice I asked for, and not the voice that was speaking a minute ago.

Marcos: Similar to fonts, you could iterate over the voices, and that’s a fingerprinting vector.

Brian: There are things that we’ve learned that we should apply here. For example, families of fonts.

Yves: Paging was a solution to make it more difficult. Don’t expect the same number of voices compared to fonts.

Brian: But the question is, is it on the device?

Lola: It’s unclear to me what the ask to the group is, here. What are we coming together for?

Marcos: Making our experience available to spec authors in the future. For example, don’t expect things to download locally. For example, Prompt API needs to download a model for whose download you have to wait before you can use it.

Heather: So the idea is to wait for Ehsan’s document, and then adopt it or make it a finding?

Matthew: We’ve spoken about the importance of the web content not being aware of where the service is being provided. Is it a concern that the user should be able to dictate where some of the stuff gets done, e.g. cloud vs. locally?

Jeffrey: I think it depends. Running in cloud can incur costs and may leak information. Both the site and the user will want input into all of that. If a site cares that they are not sending information in a way it should not be used for AI training. Users pay attention to potential costs. The site may also want to warn the user that an action may cost something. Similarly for the delays, if you need to download a several-GB button before you can use it, the site must indicate it.

Brian: We’re building lots and lots of services that integrate with browsers. Some of them are transparent. As a user, just because I happen to use browser Chrome and Android, I might want to use something other than Google as a search provider. Same with who is doing my voices. I would love to use the best available voices, I would like to choose the AI model, …. Difficult to make as all of those is another party that you’re trusting. Everything of that would be trivial to do if you had an extension. Don’t know how we can design these things. Seems to me that thinking about how you might try to prevent evil from happening, and be very clear about what you’re trusting, would be great.

Jeffrey: Sounds like there’s enough interest to write a considerations document. Not sure if all of the assumptions in Ehsan’s document are correct, e.g. device-bound. We need to go over the principles and see if we have consensus over them. Seems worth having a document.

Matthew: When Brian was speaking, the framework idea of a browser came to mind. If you could pick the particular pieces of the browser. Ehsan is also interested in the security model around extensions. Maybe that would be of interest. Know we had discussions about the fake downloads before. Another topic that seems to come up: I don’t really know if there’s a solution to it. That there are parts for an interface that people trust, and other parts which they don’t trust. Nobody except us tech people know what these bits are. Don’t know what the solution is.

Brian: Nobody is saying this cannot be a thing, enough things come through. We should think about what advice we can give. And line out what likely would not make it through TAG.

… When I discussed the proposal with Ehsan, his thinking was that one of the driving principles was that it could be updated outside of the delivery of the browser itself. Not sure what you think about it.

Jeffrey: I think that’s part of the definition. If it can’t be updated outside the browser, it’s not a component. Maybe we should have a different document if we talk about the two different cases.

Matthew (chat): +1 regarding the two different documents, we are working on a document on local vs. remote.

Jeffrey: I think we as the TAG have said things about the remote/local distinction, so I guess we would endorse such a document.

Brian: All the browsers are surface-y, they can and do vary their brinding at the OS level for those things. If you think about it, even painting windows is such a kind of thing.

Lola: Next steps?

Marcos: Let’s review the document.

(Reviewing…)

Marcos: Skyhook vs. Core Location … Leave things as a user choice … 
