# TAG Minutes - 17 Sept 2025 - Hong Kong F2F

## Web No Papers

https://github.com/w3ctag/web-no-papers -> https://github.com/w3ctag/prevent-credential-abuse

### [When standards-compliant credentials are still rejected #20](https://github.com/w3ctag/prevent-credential-abuse/issues/20)

...

Marcos: Driver's licenses are misused by acting as an identity document.

Martin: Disagree, they're _the_ identity system.

Marcos: Maybe on the web it could be different.

Lola: Relating Marcos' point to issue #20, he's saying DCs shouldn't be used for identity. Uruguay example is applicable to physical credentials. The passports didn't contain a field, so the countries decided not to accept them. How does that translate to a harm in digital credentials that's specific to digital credentials?

Martin: Good to have examples of how these systems can create exclusionary effects. As you point out, it's not specific to it being digital.

Marcos: Wasn't that it was excluding a particular group. Consequence was that.

Lola: If you happen to be in the group, suddenly you can't get to Germany or Japan just because you have the wrong country.

Jeffrey: It's about the written standard not matching what countries actually required.

Lola: Not intentionally excluding Uruguay, but it's about the system.

Sarven: Doesn't matter if it's technical or social standards. There's a standard, and they agree on it, but it gets rejected anyway. Digital credentials amplifies this, since you might just want to book a hotel room. If they look at a government credential, and it's missing the wrong optional field, they might block you. Concern is ... we can't do anything about the real world ... but in the digital space, linking identities, maybe those are useful for some people, but some don't want to do it. If the service says they can't link it because it's missing a field, it'll more easily reject things. In the technical standards world we'd normally say it's not conforming, because they do optional behavior, but it's not interoperable.

Jeffrey: The point here is twofold: you might not intend to exclude a group, but the exclusion still harms them.  We can make that point, but it's a point worth making.  Secondly, is that with physical credentials most of the time they are presented to the human who can be flexible.  Passports might be an exception because they digitized early and all passports are basically digital already.  Digital credentials never have that.

Marcos: Computers check them.  Software is written by people for people.

Jeffrey: Software is not written to be flexible.

Lola: You might make exceptions for date presentation changes.  Expiration tends to be hard.  Whereas a human might wave that through.

Martin: Even if the system could accept an expired credential, some reject those.

Jeffrey: Systems that look for fields that might not be there and fail when it isn't.

Marcos: There is a much wider concern around who issues credentials.  If you have to go to get a credential from a city if you live a long way from that city.

Jeffrey: That's in there already.

Marcos: Uruguay example isn't strong, because it was fixable at other levels. Had a consequence of excluding because of reasons, ...

Martin: RFC9413 might be interesting. Talks about what it is to have a standard. Very common situation where the practice and standard don't match. It makes the case that you need to put the work in to reconcile the differences. Doesn't say how to reconcile them. Can change practice or standards, and either is valid, but you do need to put the effort in, or the system rots. Uruguay has matched the de facto standard, but the written standard hasn't been fixed.

Jeffrey: So do we need to say that in this document?

Martin: No

Jeffrey: Agree.

Sarven: Not all technical requirements have the same impact or use. Might be specifications that help people do certain things online. With a digital credential, where it's used and implications are higher than if you can sign into twitter account. It's not that all standards have the same impact in people's lives. This has higher implications.

Lola: We have a PR open (https://github.com/w3ctag/prevent-credential-abuse/pull/47/files#diff-0eb547304658805aad788d320f10bf1f292797b5e6d745a3bf617584da017051R194) about potential specific harms. Harm of exclusion might address your concern. Harm is the potential for individuals to be excluded or marginalized when doing business or participating online. There are also other harms.

Jeffrey: Think Sarven should write a PR to fix anything that's remaining.

Sarven: Discussion was good. Got the ideas out. Initial reaction is that it's a bit short for what i'm raising, but we don't need to work it out now.

----

Martin: Next steps are that Dan's actively looking. PRs will merge mod maybe 1, which has alternatives. For the group, is this ready to approve in its current state? Recognizing that if Sarven comes up with a great PR, I want to take it.

Sarven: I think we've acknowledged the issue well, and I'll look at the spec.

Martin: Are people comfortable making this a finding, given a week for cleanup.

Jeffrey: I lean toward making the final call when everything's actually merged.

Martin: Want to make an issue cut-off.

Jeffrey: I agree with saying that, by default, this is all of the issues.

Martin: And there will be minor editorial tweaks.

Jeffrey: Also, my sense for my issues is that y'all discussed them, and if you didn't make a change for one, I trust that.

### [Harms #47](https://github.com/w3ctag/prevent-credential-abuse/pull/47)



## User Agents

https://github.com/w3ctag/user-agents/issues/

### Agreement to publish it as a draft note and echidna it?

Marcos: As long as it doesn't export the terms.

Jeffrey: I will do that.

No objections.


### PRs
#### https://github.com/w3ctag/user-agents/pull/21
#### [Drop the ecosystem section](https://github.com/w3ctag/user-agents/pull/24)

Xiaocheng: After we've stated the intended audiences, we can say that if the audiences act according to their intended behavior, we'll have a good ecosystem.

Lola: People reading this won't necessarily be technical.

Martin: Conflict of interest point is worth keeping at some level.

Lola: Line 63-67 is worth keeping.

Martin: Think that's covered by the next section, which more clearly covers the duties.

Marcos: Think the section is overly simplistic. 

Jeffrey: I hear consensus to merge this.

Sarven: No objections to dropping this section, but the document needs more of an introduction. What to expect. This section acted a bit like an introduction, but needs to be edited further. 

Jeffrey: https://github.com/w3ctag/user-agents/issues/29


#### [Add loyalty guidance for facilitating users switching UAs
#28](https://github.com/w3ctag/user-agents/pull/28)

Xiaocheng: How does this apply to in-app browsers?

Jeffrey: Says

Xiaocheng: UA shouldn't be implemented to reject market competition. Facebook in-app browser is definitely not competing with Chrome or Firefox. They're taking different slots. 

Martin: Market definition is different. But they are user agents. You can browse the web in the facebook app.

Xiaocheng: Something is still off.

Martin: The point about data portability is just one of many ways in which exercising user choice of browser might be achieved, but there are other things as well. Some are difficult. Integrations with things. Access to basic capabilities. Web compatibility. What do we want to say? Should be easy for someone to move if that's their choice. But all sorts of things stop you from changing browsers. Mostly that most browsers are bad.

xiaocheng: "User agent should not obstruct its users from switching". For example, it must not block access. 

Jeffrey: I.e. "must facilitate" -> "must not obstruct"

Martin: Think that's more practical. E.g. data portability is achieved by the target browser reading all the history, etc. Don't need to require the source browser to do something special. As much as we might aspire to standards for syncing.

Xiaocheng: E.g. I want to migrate my Copilot/Gemini history to Firefox. 

Lola: Time to go. Especially if we want to eat first.


#### https://github.com/w3ctag/user-agents/pull/25
#### https://github.com/w3ctag/user-agents/pull/27








