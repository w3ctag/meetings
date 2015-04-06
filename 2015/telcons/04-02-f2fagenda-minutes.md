# Call Minutes – 2 April 2015
## Topic: F2F Agenda Planning  

### Present: Dan, Tim, Peter, Mark, Yves
### Regrets: Travis, Yan

Chair: Peter  
Scribe: Dan  

[Agenda](https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/04-02-f2fagenda.md)

--
Topic: F2F Agenda Planning

Mark: We will be moving rooms on Tuesday and Wednesday between 2pm and 3pm due to a scheduling snafu ("mistakes were made")

Dan: Can we get flip charts?

Mark: Will look into it.

Dan: have discussed with Alex about hvaing Ilya join for a discussion on packaging.  When should we ask him to join / be there?

Alex: What other things in web performance wg could use discussion? Ilya is involved in those things. It would be good to look at what those APIs and features are or to talk with him about which ones might need review?

Dan: So Ilya for lunch and the session after on wednesday, for a discussion on web perf wg and also packaging.

Peter: Tantek and Nick Doty coming Wednesday morning for security and privacy reviews, mike west to join remotely.

Tim: for people joining remotely, can we have a big screen?

Mark: We have video conferencing in the rooms. Not sure what they will interop with – we can use webrtc.  Will bring some [kit] as well.

Peter: what's going on with Mike?

Yves: Mike will be there - he should be able to give us status report on a few things - HTML working group stuff.

Dan: Yves can you talk to mike about this and come back with a proposal.  Maybe ask Mike to present that on Tuesday afternoon.

Peter: Other guests / other topics? Anyone else we want to invite in?

Dan: Should we have a web components discussion?

Alex: We should see if Dimitri could join...

Dan: I can reach out – but is there a key issue?

Alex: I'm satisfied, but maybe others have questions...

Dan: I'm interested in what the web components lifecycle <-> standards lifecycle will look like.

Alex: There's been some stuff around [linked data and web components](http://googlewebmastercentral.blogspot.com/2015/03/easier-website-development-with-web.html)...

Alex: Dimitri is best place to discuss shadow dom and other web components specs...

Dan: I will reach out to him [to see if he can join us].

Peter: Should we talk to Alan Sterns about regions?

Alex: The regions question wrt houdini is interesting – if there is a path towards user space hosting of regions in a non-slow way and using houdini stuff – then that has some interest. And are we on track to get that done?

Dan: could we useflly use any time to move houdini along?

Peter: I can ping the Houdini chairs about it.

Dan: Maybe we could work on some targeted areas.

Peter: Box Tree API another possibility, I will reach out.

Dan: Private browsing?

Mark: I'm hoping to make some progress on that.

Dan: Ok let's put it on the agenda.

Dan: In addition: we need a slot for priveleged contexts doc. (w/ Mike West).  Do we need a follow-up discussion to https everywhere?

Dan: Tim?

Tim: How about the https without the mess?

Mark: current plan on that is opprtunistic security.

Tim: is opportunistic security a CSP like thing which is like hsts for web pages. 

Alex: That's upgrading your request. Will be in Chrome 43.

Mark: It's not opportunistic security – it's helping content producers with legacy content.

Tim: let's discuss that as well – it's being quoted by people as a solution. it's a solution for moving from http to https without breaking internal links...

Alex: if they serve the same content and they serve hsts headers then they do achieve that.

Tim: other spec is useless

Alex: that's untrue

Alex: many sites many many documents which they can't audit. Sub-resources being requested which would trigger mixed content warning.

Mark: Safari doesn't enforce mixed content; other browsers do --

Tim: Let's discuss it at the meeting.

Dan: is opportunistic encryption further being discussed in http group.

Mark: Yes.

Tim: We should have a tag [finding?] about what these things do and don't do.

Alex; We should figure out a way to document it better.

Mark: for spec reviews - it took a couple of hours – should we set aside a portion of each f2f.

Alex: yes:

Peter: agreed.

Dan: +1

Peter: anyone else we want to invite?

Mark: Some Mozilla people. 

Dan: I don't feel like we need a focused discussion on WebRTC.

Mark: I am feeling like maybe we should - particularly on the privacy and security aspects.

Dan: Maybe part of the spec reviews discussion - what ought we to be doing on webrtc?

Dan: should we have like a general what the TAG is doing ... how we work ... what role we play, especially in how W3C starts new work...

Mark: Yes

Dan: Ok will add that.

Mark: Robin is doing his whole tooling refresh efforts. Is that something of interest or not in scope?

Peter: I've been following it but not sure if it's in scope for the TAG.

Dan: Maybe sometime between now and next f2f...

[discussion on the next f2f]

Mark: had a discussion with wendy / webapop sec chairs about europe f2f dovetailing with next f2f - a possibility
