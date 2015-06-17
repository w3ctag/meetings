
##CSV "On the Web"

JeniT
4 issues I'd like TAG opinion

##1. Meta-data associated with the file
* Largely discussed last week. Making progress on it.

##2. How to refer to files (of a particular type) when format/media-type is unknown

We have a conversion mechanism (CSV->Other format). We want to say how to do that conversion, optionally with a template. (see \url{http://w3c.github.io/csvw/metadata/#transformation-definitions)}

We specified URLs instead of media-types. Would love feedback on this decision.

Hadley: 
    I think this is the right direction. Not sure we could list all vocabularies, types, etc., seems hard to keep up.
I like future-proofing the spec to make this more practical.
I recognize this is a depature from more standard policies

MNot:
    Since media-types are extensible, and easy to register... not sure I agree.
    If everything can become a URI, how far do we take it (not every integer would get a URI)
    Central question: Is this strongly-typed as a media-type. Is it expected that we'd put other things in it, or is it just for formats?
    
JeniT:
    Well, it gets funny around the edges... How granular do you go with media-types, and descriptions. 
    Is it possible for 3rd party to define media-types?

MNot:
    Given the new process, any group can go register and add a media-type.
    In this particular issue, it's not so cut-and-try. (Could be either way.)
    If you are asking the TAG, what they think, it could be a bigger issue (what direction should we go).
    I don't want to block your spec; I think coming up with this larger direction will take a lot more time.
    
Hadley:
    Registration is still a particular hurdle. Might be one more point of friction.
    I hadn't realized just how easy it was to register a mime-type
    
MNot: 
    We should be careful not to go too far. Interop can suffer. There's a balance there.

JeniT
    The push against URL is what is the cannonical type? Mime-types give you that.
    
PLinss:
    I'm a little reluctant to tell someone not to use a media-type for something that clear is (unless there's a reason they flat-out won't work)
    
Travis:
    Also inclined toward media-types. Cites various media-types used in Media containers.
    
Alex:
    URLs also a little more brittle for DNS changes, etc.
    
JeniT:
    I'll take that as a somewhat unanimous concensus.
    
DavidB:
    No opinion.
    

##3. FYI (no specifc action required) CSV->RDF we want to use link relation (describe, registered with IANA) as a URL. Yet there's no particularly-defined URL for such.

JeniT:
    Not all link relations have a URL. Many do (coming from HTML), but this one is causing a bit of a problem.

MNot:
    I think we have a resolution for this. RFC brewing...
    Some URLs won't recognize equivalence in link relationships.
    
JeniT:
    Is this likely to resolve in a few weeks? :)
    
MNot:
    No. Maybe expect this in a few years given its relative priority.
    Get a discussion going on Github, we can pre-arrange for it from there.
    Could be a hash URI, individual pages?
    
JeniT:
    Our intention is to define it in our own Namespace and then define an equivalent relationship once the official one is published.
    I'd rather do the above, then define it in a someone else's namespace.
    
##4. URL Equivalence

JeniT:
    We want to be able to test whether the URL in the meta data is the same as the URL in the file?
    \url{https://github.com/w3c/csvw/issues/562}

   * What should we use to do a URL equivalence.
   * 
Hadley:
    Reminded me of the https conversation at last F2F, and how/if this messes up the equivalence with non-https sites. Do these represent the same resource independent of the protocol?
    Short answer: I'm not sure. We have some work to do.
    Might be a topic for Berlin (next F2F)

David:
    I've seen this problem before. When we wanted to test equivalence in a feature in CSS, we ended up dropping it because we couldn't define it.
    I'm not sure anyone has written this down.

JeniT:    
    RFC 3986 has a definition for URL. We could point at that.
    
MNot: 
    Back in the sands of time, this was described somewhere, but may not be relevant anymore?

JeniT:
    Will anyone object if we reference the RFC and reference the normalization based on that?

Hadley:
    No, I think it shouldn't block you from publishing. The world needs this spec!

PLinss:
    Seems reasonable.

Alex:    

   * So I have a meta question, sort of touched on last week: all these specs seem to imply that browser integration will happen at some far removed
   * I love that this stuff is being speced.
   * It seems like it should be made easier in a browser.
   * 
JeniT:
    As noted last week, its outside the charter of this work. We did talk about it, and decided to see what it's use will be, before considering rechartering to bring browser APIs into scope.
    I want to see a bit more experimentation first.
    
Alex:
    I sympathise.
    
JeniT:
    I think a lot could be done with web components as far as experimentation. Then we'll see.
    
<End of CSV Conversation>

Topic:
#Security Questionaire
\url{https://w3ctag.github.io/security-questionnaire/}

PLinss:
Where and how we publish this.
Should be have dated versions?
Suggested to publish as a Note?

Hadley:
    Will this be manditory? What do we expect people to do with it?
    I don't have any objections to putting it out in TR space.

MNot:
    We had one spec try out using it.
    Wonder if this was useful for them? How it work?
    Where is it in the process?
    
Hadley:
    I worry that putting it in TR space is shorthand for legitimizing it.
I don't want publishing this to create the perception of more bureaucracy

David:
    Suggests using the SOTD section to describe what the status is. :)
    
Travis:
    Did we agree to own that document? I think so...
    
Plinss:
    The value of the Note is that it gives the document a stable URL.

Travis:
    I don't see too much of a problem with publishing as a Note with an appropriate description of what we think about this document (that we intend to update often).
    
(General agreement)

Alex:
    I would like for us to lend our support to efforts that can help improve specs and which we might use in the process of reviweing specs
this document seems to fit both bills

Hadley:
    I'm a little worried about the potential tarnish on our reputation if this isn't developed into something mature. But otherwise, I'm behind this with an appropriate status section (to set expectations).

To publish?
MNot+1
Hadley+1

Plinss:
Who's going to write/update the status section? Who's the point person on the TAG for this?

MNot:
    I nominate Yan.

*Resolution: Yan Zhu to publish security questionaire as a Note with a newly updated status section.

(Adjurned)

