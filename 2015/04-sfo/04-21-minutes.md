## W3C Technical Architecture Group face-to-face
### - DRAFT -
### April 21 2015

###   Intros from new TAG members

Travis: my background is more on the programming, object-model, JavaScript side, rather than CSS
... super-excited to be here
Yan!: Work at Yahoo! and the Security! Engineering! team; working with EFF! on a new Certificate! Authority! called Let's! Encrypt!
Hadley: Chair of Data on the Web WG; my main interest is in what we call "data"; working with UK government
Tim: Spent time trying to get people to not just write technical specs but also to [write up other stuff]
Hadley: Most of the decision makers and policy makers are not technologists
Mark: Australia, government discussions… people have very little context, and they make judgements based on metaphors
Yves: 1994 I implemented my first HTTP implementation, CSS implementation after that
Peter: Implemented NgLayout gecko  layout engine  
Alex: Trying to make the Web a real application platform
Mark: I work on HTTP
Tim: I am 100% American and 100% British
Dan: I live in London but I'm all American
... I got into this gig because originally I was… my first interaction was when I was maintaining WWW library pages
... more recently I've been involved in mobile stuff, and [even more recently] some FirefoxOS involvement

# Proposed French intelligence bill

[Yves gives some background]
Yves:: W3C announced on twitter that we are opposed to pervasive surveillance [and concerned about this bill]
... Does the TAG want to take a position on this?
Dan: Link to Montevideo statement?
Yves: they want to put "black boxes" in ISPs etc that sniff all traffic
Mark: cynically this is more incentive to deploy encryption
Tim: interesting case of finding balance between legal solutions and technical solutions
... but encrypting things doesn't actually solve the problems
... somebody stting there watching your traffic, they can't see your encrypted data but they know what you're doing
... [what sites you're visiting, etc.]
Yves: warn about the pitfalls of pervasive surveillance?
Mark: not sure what we can say about [the checks and balances]
Dan: Encryption mitigates against pervasive monitoring
... it takes an impliict policy position vs pervasive monitoring
Hadley: Can we articulate why we believe surveillance is bad technically? [as opposed to ethically or morally]
Tim: There are some technical parts that we can say something about
... We use the Web as a file system—calendar, etc
Travis: So it's disruptive to [normal user experience of the Web]
Tim: So much breaks [when you start messing with stuff in this way]
Alex: But that's still not really technical
Alex: The way TCP works… anything not [explicitly disallowed] is allowed
Alex: I can't argue against it technically; I have to make an argument that's socio-political
Mark: the strongest argument… create a playing field.. "Tussle in Cyberspace"
\url{http://dl.acm.org/citation.cfm?id=1074049}
Tim: You're at the W3C. We can argue that we are making the world better
... that can be our starting point
Mark: I wonder how the membership will react to that
Tim: If you don't start out with that… you can end up with this great gaping sore in the system
Alex: I am also unconvinced that the IETF just hasn't chosen to ignore the question for as long as possible
Mark: My impression is that situation is starting to fall apart [and that there's a realization that this is about human rights]
Dan: I think there's more ideology there than what you imply
Dan: I want to come back to the STRINT workshop
Dan: Scopiing this discussion back to the current France thing…
Hadley: About the user focus
... the argument that the Web won't work [if people can't trust it]
... there are countries who think the role of government is to keep an eye on people to keep them safe
Tim: We can say lots of things about what the characteristics are of a functional Web without [infringing on any of that]
Dan: So Yves what are you suggesting you the TAG do?
Yves: Well there is a petition online
Yves: when the W3C speaks as W3C, the issue is that we are speaking for all W3C members
... but the TAG is a separate entity [which can take its own positions, not necessarily speaking on behalf of the entire W3C]
Mark: I'm wondering if having the TAG say it's against pervasive monitoring… does it cause heartburn for you, Hadley?
Hadley: I'm struggling to see what the technical argument is
Alex: We could make recommendations about what user agents should be doing
... e.g., there is movement to have Chrome give users an indication [in the browser UI] that HTTP is insecure
... [when they are visiting a site using non-TLS http]
Yan: We can say "Don't make new features usable over [non-TLS] http"
Dan: [mention about US gov moving to https]
Mark: Patting the government on the back is a relatively easy thing to do
Dan: I'm talking about giving out some carrots instead of just smacking the French government with a stick
Mark: Once we start going after governments, where do we stop? Do we go after Thailand next?
Yves: It's not about being against the French government; it's about using [this as an opportunity to make a clear position]
Hadley: Everything we're talking about is a bit more nuanced than we can fit into 140 characters
...You get government attention when you point out
... 1. this will hurt something else you care about
... 2. this will cost you a lot of money and it will turn out to be a big waste [in the long run]
... 3. this will cost you votes
Dan: What about number 2?
Yves: Economic consquences… we know that hosting services have moved outside of the US to escape PRISM
... like what happened with the banking system when Switzerland established itself as a place where [you could bank anonymously]
... [we will have places like Iceland which will become hosting centers because people can trust they won't get in the way]
Dan: Maybe we could give them a nudge… to point out, "This isn't going to work"
Dan: We can point out that the trend is clearly toward more encryption
... that's a technical argument we could make
Alex: We could end up with shadow legislation
... requirements that happen out of view
Dan: What about number 1?
... pointing out that this hurts democracy, and that these specific institutions in government are damaged by pervasive monitoring
... or that it damages the economy
Alex: Folks who sniff don't care about that
Dan: Is there something from all of this that we can distill down?
Dan: Question for Yves… the option of just signing something… what is that thing we would sign?
Mark: What is the likelihood of this passing? Does it have strong support?
Yves: The decision will be made by May 5… the original vote was just made by a group of 30 legislators [because they were the only
... ones who showed up to vote]
Yan: Doesn't the law have multiple parts?
... and some of those parts we might not want to speak to at all
Yves: The range of the law is quite large
... it includes penalties for [whistleblowers like Snowden]
[TAG scrolls through through the petition together]
Dan: Maybe we could just do a blog post?
... going back to the STRINT workshop
... saying that pervasive monitoring is an attack against the Internet the undermines it
Mark: and saying that people need to engage with their legislators, get involved
Hadley: We in government and we [in the the W3C] are both building something for the future
... we have this constructed tension… that tension is healthy
Mark: The technical half is important… but it works within a context [that is not technical]
Tim: We have to be careful about not getting sucked down the Snowden Vortex
… everything gets turned into [a discussion about Snowden]
Dan: I'm hearing that we need to do a blog post, talking about what the technical community is doing, and recommending
... that people get involved
Mark: Yeah [can talk about France but we also want to get the message out to others]
Dan: Should we mention non-governemental orgs like EFF?
Hadley: I think our message should be our message
ACTION: Mark to draft a blog post within the next day or so
Alex: Who's the audience?
Hadley: People pay attention to the W3C when they're trying to figure out what to do
Dan: It helps us figure out our own work plan
… it's a concrete statement that helps to keep the momentum going on the position we've already taken on encryption
... and it could give some support to the people in France who are fightling against the intelligence bill
Alex: If that's the case, maybe we should talk to some of those people [and that will inform what we write]
Alex: where does the document go? what's the messaging plan around it?
Hadley: I will be happy to help with writing it
[Brian Kardell joins the meeting]

# IETF and HTTP
Mark: IETF met in Dallas; Peter attended
... we are publishing HTTP2 [as an RFC soon]
... we have some other smaller things we're working on
... "Alternative Services"… Firefox has implemented it [but is not shipping it yet]
... and Opportunistic Security [Encryption?], for transparently upgrading the connection to TLS without the origin changing
Mark: Only Mozilla is implementing Opportunistic Encryption [not shipped it]
Alex: [We on the Chrome team are adamently against Opportunistic Encryption because it doesn't solve any problems]
Mark: The IETF is generally enthusiastic about Opportunistic Security
Mark: The W3C is much less excited about Opportunistic Security
Yan: Alt Service is useful without Opportunistic Encryption?
Mark: Yeah, they are completely separate specs
Mark: there's also a new  Tunnel Protocol for Connect spec [header name is ALPN]
##[Draft HTTP Extension Specifications](\url{https://github.com/httpwg/http-extensions#draft-http-extension-specifications)}
Mark: TCP… discussion about UDP-based application protocols [mentions QUIC]
... we are probably going to start talking about a UDP-based HTTP in the near future
... and we need to consider middle boxes
... SPUD is a protocol proposal that's come from Cisco
... adding a metadata channel outside of an encrypted flow
... there are benign uses of that, and there are [less benign uses]
... some of this stuff potentially changes the properties of the Internet as we know it
Mark: [about the UDP stuff] people are fully aware that some of this new work amounts to re-inventing many features of TCP
Mark: We are holding a workshop in July, in Germany, the week after [something]… by invitation, with people submitting position papers
Mark: there is a spec from Google, and it's implemented in Chrome
... there was a spec for SPDY at the time it was being developed and I was able to implement from that spec pretty quickly
... but the spec for QUIC is not yet of that level of quality such that I would independently implement from it
</green>

[Lunch concludes]

# Houdini 

Alex: Theer is a long-running challenge - imagine doing CCS regions in user \_\_ \_-- you eant to cancuate is inrinctsic width rather tan minwidth --- imagine ehwn you have to do tos ecaculations... You can use htings like th fonts. You want to avoid doing that inthe docuent befoe you actually insert the frame... you wan  to know what the size of the frame would be if it were inserted.  Lots of areas whether you want to do cascading style --- you need an API which will allow you to cooperate with the style resolver  and take things into your own hands.

Text measurement is it own part of this ... if you do something like GoogleDocs where yo doi all your own layout and line-breaking, you need this.     Text is going to have its own APIs in this area.

Suppose you had Illustrator in the browser taking a font and turning into art.   Or you biuld your own 3D renderer for generating fonts [missed]

HTML 5 AND STUFF

Mike:  Robin B, a few years ago, as hired to be the editor of the W3C version of the HTML spec.  Hixie was still the editor on WHATWG.  I was staff contact.  When Hixe resigned from being the edito, and so did Majek @@ and so did I .... Robin was paid under contract from MS Google and Adobe.  I put a lot of workingt o making sure we kept Robin on.     

Then we got to Rec.  Now we have a plan to do dot releases (as in origibnal plan) but a lot of things have changed.  It is becoming clear that the syrcuctrue of the WG is non-optimal.  Scope creep is what we do best ==> HTML scope is now crept. 
We have had some discussions with some of the people who have been supporting the work for a long time.

[..]

We are also going to "modularise" the HTML spec (no relation to XHTML modularization).   Lots of the HTML spec isn't so much about te HTML language as about how you actualy load web pages.

Robin has made it much easier for more people to contribute to the spec.  He has set up a github repo, people can edit the specs in github. 

Travis: There is a general culture in the WHAT WG of "oh, I have a great idea -- I will ask the WHATWG editor to write it up".   Here is an alternative, that you just do it yourself.  

This begins by someone just writing it up.  Then in future they could come to a new Incubator community group. That would take it in, and either do it or get a WG to do it [??]

We can't take just any work into the HTML WG, or especially the Web App WG, with more restrictive charter.

DKA: How do others feel about this process?

Alex: Cautious about process changes ion th is area. We do need changes -- big ones.    We need to address why the W3C spec is infereior to the WHATWG 


he table sorting algo like many things in fact is  which are badly designed  — just like the sorting algo snot what people actuall need or use…  Similarly other things  like meaning of name, section etc .. so the overall quality of the work in whatwhg is low ,  ut why is it w3c where things happens

Tim: Compromse good/fair/fast -- drop any one and you can do well on the others.  
Alex: but if w3c is slow, it shjould be more good

Brian :  Can we use custom element demos as a way toward standards?

DKA:   YEs, for some things, but there are other things which you cannot acheive using 

Mike: Example i sthe picture element — tis waa soemthing people wanted — responsive pictures — thta came from developers. 

    Brian: They first implemented  it — crowdsourced — kickstarter — an implementation in JS then they hacked it into the browser code.
    
    DKA [draws flow diagram  -- to idea ->  make custom element -> get experience -> 

[switch to IRC]

ACTION: Travis to write some feedback on the work of the html accessibility task force work on focus navigation and activation...

Mark: have we moved on from a keyboard and a screen? What is the abstraction?





