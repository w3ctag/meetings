## W3C Technical Architecture Group face-to-face
### - DRAFT -
### April 21 2015

### Contents

* Intros from new TAG members
* Proposed French intelligence bill
* IETF and HTTP
* Draft HTTP Extension Specifications
* Houdini
* HTML5'n'stuff
* Interaction Events
* CSS Regions Draft Feedback
* Captive Portals

[#tagmem IRC Log from this day](http://www.w3.org/2015/04/21-tagmem-irc)  
[Agenda](https://github.com/w3ctag/meetings/blob/gh-pages/2015/04-sfo/agenda.md)

Present: Daniel Appelquist, Hadley Beeman, Tim Berners-Lee, Yves Lafon, Travis Leithead,  Peter Linss, Mark Nottingham, Alex Russell, Yan Zhu

Guests: Mike Smith (all day); Chaals (for discussion on Interaction Events); Alan Stearns (for discussion on CSS Regions); Brian Kardell (for discussions on Houdini and HTML5)

Chairs: Dan Appelquist, Peter Linss

Scribes: Mike Smith, Tim Berners-Lee

### Intros from new TAG members

Travis: my background is more on the programming, object-model, JavaScript side, rather than CSS
… super-excited to be here

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
… I got into this gig because originally I was… my first interaction was when I was maintaining WWW library pages
… more recently I've been involved in mobile stuff, and [even more recently] some FirefoxOS involvement

### Proposed French intelligence bill

[Yves gives some background]

Yves: W3C announced on twitter that we are opposed to pervasive surveillance [and concerned about this bill]
… Does the TAG want to take a position on this?

Dan: Link to Montevideo statement?

Yves: they want to put "black boxes" in ISPs etc that sniff all traffic

Mark: cynically this is more incentive to deploy encryption

Tim: interesting case of finding balance between legal solutions and technical solutions  
… but encrypting things doesn't actually solve the problems  
… somebody stting there watching your traffic, they can't see your encrypted data but they know what you're doing  
… [what sites you're visiting, etc.]  

Yves: warn about the pitfalls of pervasive surveillance?

Mark: not sure what we can say about [the checks and balances]

Dan: Encryption mitigates against pervasive monitoring  
… it takes an impliict policy position vs pervasive monitoring
Hadley: Can we articulate why we believe surveillance is bad technically? [as opposed to ethically or morally]

Tim: There are some technical parts that we can say something about  
… We use the Web as a file system—calendar, etc

Travis: So it's disruptive to [normal user experience of the Web]

Tim: So much breaks [when you start messing with stuff in this way]

Alex: But that's still not really technical

Alex: The way TCP works… anything not [explicitly disallowed] is allowed

Alex: I can't argue against it technically; I have to make an argument that's socio-political

Mark: the strongest argument… create a playing field.. ["Tussle in Cyberspace"](http://dl.acm.org/citation.cfm?id=1074049)

Tim: You're at the W3C. We can argue that we are making the world better  
… that can be our starting point
Mark: I wonder how the membership will react to that

Tim: If you don't start out with that… you can end up with this great gaping sore in the system

Alex: I am also unconvinced that the IETF just hasn't chosen to ignore the question for as long as possible

Mark: My impression is that situation is starting to fall apart [and that there's a realization that this is about human rights]

Dan: I think there's more ideology there than what you imply

Dan: I want to come back to the STRINT workshop

Dan: Scopiing this discussion back to the current France thing…

Hadley: About the user focus  
… the argument that the Web won't work [if people can't trust it]  
… there are countries who think the role of government is to keep an eye on people to keep them safe

Tim: We can say lots of things about what the characteristics are of a functional Web without [infringing on any of that]

Dan: So Yves what are you suggesting you the TAG do?

Yves: Well there is a petition online

Yves: when the W3C speaks as W3C, the issue is that we are speaking for all W3C members  
… but the TAG is a separate entity [which can take its own positions, not necessarily speaking on behalf of the entire W3C]

Mark: I'm wondering if having the TAG say it's against pervasive monitoring… does it cause heartburn for you, Hadley?

Hadley: I'm struggling to see what the technical argument is

Alex: We could make recommendations about what user agents should be doing  
… e.g., there is movement to have Chrome give users an indication [in the browser UI] that HTTP is insecure  
… [when they are visiting a site using non-TLS http]

Yan: We can say "Don't make new features usable over [non-TLS] http"

Dan: [mention about US gov moving to https]

Mark: Patting the government on the back is a relatively easy thing to do

Dan: I'm talking about giving out some carrots instead of just smacking the French government with a stick

Mark: Once we start going after governments, where do we stop? Do we go after Thailand next?

Yves: It's not about being against the French government; it's about using [this as an opportunity to make a clear position]

Hadley: Everything we're talking about is a bit more nuanced than we can fit into 140 characters  
…You get government attention when you point out  
… 1. this will hurt something else you care about  
… 2. this will cost you a lot of money and it will turn out to be a big waste [in the long run]  
… 3. this will cost you votes  

Dan: What about number 2?

Yves: Economic consquences… we know that hosting services have moved outside of the US to escape PRISM  
… like what happened with the banking system when Switzerland established itself as a place where [you could bank anonymously]  
… [we will have places like Iceland which will become hosting centers because people can trust they won't get in the way]  

Dan: Maybe we could give them a nudge… to point out, "This isn't going to work"

Dan: We can point out that the trend is clearly toward more encryption  
… that's a technical argument we could make

Alex: We could end up with shadow legislation  
… requirements that happen out of view

Dan: What about number 1?  
… pointing out that this hurts democracy, and that these specific institutions in government are damaged by pervasive monitoring  
… or that it damages the economy

Alex: Folks who sniff don't care about that

Dan: Is there something from all of this that we can distill down?

Dan: Question for Yves… the option of just signing something… what is that thing we would sign?

Mark: What is the likelihood of this passing? Does it have strong support?

Yves: The decision will be made by May 5… the original vote was just made by a group of 30 legislators [because they were the only  
… ones who showed up to vote]

Yan: Doesn't the law have multiple parts?  
… and some of those parts we might not want to speak to at all

Yves: The range of the law is quite large  
… it includes penalties for [whistleblowers like Snowden]

[TAG scrolls through through the petition together]

Dan: Maybe we could just do a blog post?  
… going back to the STRINT workshop  
… saying that pervasive monitoring is an attack against the Internet the undermines it

Mark: and saying that people need to engage with their legislators, get involved

Hadley: We in government and we [in the the W3C] are both building something for the future  
… we have this constructed tension… that tension is healthy

Mark: The technical half is important… but it works within a context [that is not technical]

Tim: We have to be careful about not getting sucked down the Snowden Vortex  
… everything gets turned into [a discussion about Snowden]

Dan: I'm hearing that we need to do a blog post, talking about what the technical community is doing, and recommending  
… that people get involved

Mark: Yeah [can talk about France but we also want to get the message out to others]

Dan: Should we mention non-governemental orgs like EFF?

Hadley: I think our message should be our message

ACTION: Mark to draft a blog post within the next day or so

Alex: Who's the audience?

Hadley: People pay attention to the W3C when they're trying to figure out what to do

Dan: It helps us figure out our own work plan  
… it's a concrete statement that helps to keep the momentum going on the position we've already taken on encryption  
… and it could give some support to the people in France who are fightling against the intelligence bill  

Alex: If that's the case, maybe we should talk to some of those people [and that will inform what we write]

Alex: where does the document go? what's the messaging plan around it?

Hadley: I will be happy to help with writing it

[Brian Kardell joins the meeting]

### IETF and HTTP

Mark: IETF met in Dallas; Peter attended  
… we are publishing HTTP2 [as an RFC soon]  
… we have some other smaller things we're working on  
… "Alternative Services"… Firefox has implemented it [but is not shipping it yet]  
… and Opportunistic Security [Encryption?], for transparently upgrading the connection to TLS without the origin changing

Mark: Only Mozilla is implementing Opportunistic Encryption [not shipped it]

Alex: [We on the Chrome team are adamently against Opportunistic Encryption because it doesn't solve any problems]

Mark: The IETF is generally enthusiastic about Opportunistic Security

Mark: The W3C is much less excited about Opportunistic Security

Yan: Alt Service is useful without Opportunistic Encryption?

Mark: Yeah, they are completely separate specs

Mark: there's also a new  Tunnel Protocol for Connect spec [header name is ALPN]


###[Draft HTTP Extension Specifications](https://github.com/httpwg/http-extensions#draft-http-extension-specifications)

Mark: TCP… discussion about UDP-based application protocols [mentions QUIC]  
… we are probably going to start talking about a UDP-based HTTP in the near future  
… and we need to consider middle boxes  
… SPUD is a protocol proposal that's come from Cisco  
… adding a metadata channel outside of an encrypted flow  
… there are benign uses of that, and there are [less benign uses]  
… some of this stuff potentially changes the properties of the Internet as we know it  

Mark: [about the UDP stuff] people are fully aware that some of this new work amounts to re-inventing many features of TCP

Mark: We are holding a workshop in July, in Germany, the week after [something]… by invitation, with people submitting position papers

Mark: there is a spec from Google, and it's implemented in Chrome  
… there was a spec for SPDY at the time it was being developed and I was able to implement from that spec pretty quickly  
… but the spec for QUIC is not yet of that level of quality such that I would independently implement from it  

[Lunch break]

### Houdini 

Alex: Theer is a long-running challenge - imagine doing CCS regions in user \_\_ \_-- you eant to cancuate is inrinctsic width rather tan minwidth --- imagine ehwn you have to do tos ecaculations… You can use htings like th fonts. You want to avoid doing that inthe docuent befoe you actually insert the frame… you wan  to know what the size of the frame would be if it were inserted.  Lots of areas whether you want to do cascading style --- you need an API which will allow you to cooperate with the style resolver  and take things into your own hands.

Text measurement is it own part of this … if you do something like GoogleDocs where yo doi all your own layout and line-breaking, you need this.     Text is going to have its own APIs in this area.

Suppose you had Illustrator in the browser taking a font and turning into art.   Or you biuld your own 3D renderer for generating fonts [missed]

### HTML 5 AND STUFF

Mike:  Robin B, a few years ago, as hired to be the editor of the W3C version of the HTML spec.  Hixie was still the editor on WHATWG.  I was staff contact.  When Hixe resigned from being the edito, and so did Majek @@ and so did I …. Robin was paid under contract from MS Google and Adobe.  I put a lot of workingt o making sure we kept Robin on.  
…Then we got to Rec.  Now we have a plan to do dot releases (as in origibnal plan) but a lot of things have changed.  It is becoming clear that the syrcuctrue of the WG is non-optimal.  Scope creep is what we do best ==> HTML scope is now crept.  
…We have had some discussions with some of the people who have been supporting the work for a long time.  
[…]  
…We are also going to "modularise" the HTML spec (no relation to XHTML modularization).   Lots of the HTML spec isn't so much about te HTML language as about how you actualy load web pages.  
…Robin has made it much easier for more people to contribute to the spec.  He has set up a github repo, people can edit the specs in github.

Travis: There is a general culture in the WHAT WG of "oh, I have a great idea -- I will ask the WHATWG editor to write it up".   Here is an alternative, that you just do it yourself.  
…This begins by someone just writing it up.  Then in future they could come to a new Incubator community group. That would take it in, and either do it or get a WG to do it [??]  
…We can't take just any work into the HTML WG, or especially the Web App WG, with more restrictive charter.

DKA: How do others feel about this process?

Alex: Cautious about process changes ion th is area. We do need changes -- big ones.    We need to address why the W3C spec is infereior to the WHATWG 

he table sorting algo like many things in fact is  which are badly designed  — just like the sorting algo snot what people actuall need or use…  Similarly other things  like meaning of name, section etc … so the overall quality of the work in whatwhg is low ,  ut why is it w3c where things happens

Tim: Compromse good/fair/fast -- drop any one and you can do well on the others.  

Alex: but if w3c is slow, it shjould be more good

Brian :  Can we use custom element demos as a way toward standards?

DKA:   YEs, for some things, but there are other things which you cannot acheive using 

Mike: Example i sthe picture element — tis waa soemthing people wanted — responsive pictures — thta came from developers. 

Brian: They first implemented  it — crowdsourced — kickstarter — an implementation in JS then they hacked it into the browser code.
  
DKA: [draws flow diagram]  -- to idea ->  make custom element -> get experience -> 

Brian[?]: the table sorting algo like many things in fact is which are badly designed — just like the sorting algo snot what people actuall need or use… Similarly other things like meaning of name, section etc… so the overall quality of the work in whatwhg is low , ut why is it w3c where things happens  
…Example is the picture element — is soemthing people wanted — responsive pictures — that came from developers.

Alex: If you don’t implementers involved then your ideas are toast. SO having a single CG is interesting a a place to connect with implemnters. There can be push and pull - the CG could look at news from frameowrks fetures..

DKA: so we should steer people with new ideas to the CG” [yes]

Travis: The CSS WG seems actually to work kinda like this inside the CSS WG itself — very effectively.

Mike: Webapps works in fact quite like this too, with subgroups working on different ideas. WebAppSec too.

Mike West is prolific and also gets people implementaing things.

Mike: Th emodel with going to Hixie worked often — yes there were some mistakes like AppCache, but there weer

Alex: we have got by by the heroic efforts of a few individuals — I would like standards much more boring.

Mike: Where to the bug fixes go when we find them? Also important question Hixie can fi xbugs, and he does talk to implementers.

Alex: I reemebre the table sporting thing — we loked at the proposal and said it would not fly but our feedaclk was not taken into account

Hadley: Bad to have a single point of failure in th e process

Mike: Much less so now.  
… we have an editor but we can have multiple editors  
… The supposed division between whatwg and w3c never existed — I know — I ewas originally whatwg and many like me have feet on many places. don’th think people were super happe with the way worked in the whatwg — we do need to make a new workmode which focusses on real collaboration.  
… I always try to get people to make tests and reveiw them. There are only 5 people who review thos specs. Very hard to get people to write test cases.  
… People don’t have time.  
… We need people to contribute in reasonable chucks of time.

Alex: Important that powerful people don’t have the influence to bring in features without proper consideration and review. Browse makers eg have power. Should not hust implemeht thing hat sem a good idea at atime.  
…The community group is a better model allow reveiew, and prioritizing new work.

DKA: So, should we tell devs about this new peocess, to use it for their new ideas? Is there a TAG role there?

Travis: Sounds very relevant

Mike: This is one idea … it isn’t baked .. and this is a multi-stakeholder concortium. Very early … not discussed with many place slike AB and AC.  
… will be discussed in many places.

Hadley: role of TAG here? We don’t want to be in the critical path and slow things up

Alex: Blink team now has a proces for puting things into the product, which connects to te diagram on the board — trout simming upstream … The TAG shoudl be involved with new work decisions at W3C in general.

[agenda shuffling]

DKA: I think you Mike should take positive energy nack to PLH

Mike: You should hear all this from Robin — he is largely responsible for many of the ideas here.
… Let’s have some sort of meeting about this sround the AC

### Interaction Events 

Charles: A basic problem isth athe way in which user interaction happens is basically borken…
If you have links, buttons and forms - things moe or less work…
If you want moderately useful keyboaord interaction, for example in paicular — you often write a crap tonne of js which doesn’t quite work…

Tim: Like entreing mumbers on a over-cure bank site?

Ch: more like bowser grabbing the keys which yor web site want to do use as key input  
… what we try to do s get devs to write interfaces for users… and most of he time they do a not good job

Travis: Conflict between having useful keyboard shortcuts in the browser vs allowing devs to use absolutely evertything

Ch: I know about this from the 90’s . The attention evnts TF wrk is an ettempot to clean this up — a bit  
… Work to define things with ARIA today is - you describe the roles, which is useful, then you agsin write a ton of borken JS.  
… One apporach is — to define richer things in ARIA which define behaviour and you ask the bowsers write code which works in the enviroment.

Travis: We reseve spaces fo rextensibility but not for accessibility. Like X -mfr-css-tags  
… but whe it comes to safe space ther is non in ion Accy.

Ch: If you use Accesskey, then all the access keys we have today, except that the browser can map things to other keys —  
…you can’t predict in advance and no discoverability with an API what keys are grabbed by the browser or the OS

Travis: AND we now hve special keystroke-subversion APIs

Alex: The counterfactual.  
…IS AcessKey godo for you because you think it is available, or because it is easier for authiors, or because it doesn’t involve script?

Ch: All the above  
…Keyboard navigation w/o the acces key consists of moving the tab button to move though all the 500 buttons in your email page  
…Opera didn’t do that — but then so many ppages said “use the tab key” that Opera had to chnage

Charles: Access key is not briolliant but works

___: Screen readers can pull out access keys — and tell a screen reader what is available.

Ch: Opera — pressing dot “.” would pop up a menu of access keys, which you wcould work from te menu or just use the key  
…Worked better than any other browser

Charles: Do not standradize keys whcioh many pages us incommon, craete a higher level abstraction. Like “mark mail as spam” as a browser gnerated standard event

Alex: When desiging a rich test editor, mapping the processing of keys was complex.  
…There is a cintrioller which generates data which generates view — but I havce access to none of these.

Alex: Does accesskey allow you to specift combinators?

Ch: It allows you to specify a space separeted list of characters, and it expects its chosen accelerator to be used with teh first one on th list  
…Interesting problem here is - how to simple devs write a simple system which works? Never much high end complex frameowrks.

Alex: Well, how about common ground bwteen those use cases?

DKA: If an app could query the situation, it could adapt.

Charles: Brokenness: only spec one character. Can’t change the modifier. Can’t specify a voice-command command.  
…The webapp should be able to request a set of controls — in some cases to be tolod it can’t get it
…The consistency shoiuld be primarily across web pages for the same browser, not across browsers for the same web page.  
…ARIA things are more bakes than random tstuff in a new web app.  
…and more baked than thinks in HTML.  
…Does havingthings like “Copy” defined help? Having that extensible?  
…Ideally yyou can define as many as you [the dev] wants.
…There is a conflict avoidance mechanism.  

Travis: Can you talk about Intention events?

Ch: When you want to do text input, you say “input this text”, “sel;ect these things”… things like “mark as spam” “scrooll ul” you woudl be able to colelct the event from the borwser.

Ch: You must have locally defined event types within the app, which would never be standardized.

Hadley: https://www.w3.org/WAI/PF/HTML/wiki/Keyboard

Alex: To what extent can we do things like reflct what has been registered at each levels, without an API?

CH: If you ha an API, say document.shortcuts, defdined say as the value of te accesskey taken from the attributes. Shortcuts trigger something amd it is useful to be able to give something a name.  
…In ARIA you have algos to find a name which you can present — say to soemtone wondering what would happen when click on a button.  
…The other question i whether the brower feeds back the application … the author on a good day knows the app better than the browser, and so the web app should be able to getthe info as to what is reserverd, so it can resolve conflicets.  
…There is a kinior fingerprinting use — not that many combos

Alex: When sommehting goes fill screen, how much tof the browser handling of this should be suppressed as it startt s to become a full scree app in its own right?  
…Sophisticated applications could provide diffeme shortcuts as a function of which mode [context] you are in

Ch: yes it must be totally dynamic

Alex: Has anyone charted the path of a keystroke thoughtout the whole sequence of events?

Travis: The DOM Tree events spec has been hard largely from this stuff being so unkown

Do registered access keys wehn presed also generat ethe kedown/up/pressed events?

Brian: Not in Chrome — I just tried it

Ch: I have used event.accesskey and it works at least in some bowsers

Travis: Hard to find a model which maps access keys to keyboard events

Alex: There is implicit action for acces keys? like on a A tag it follows the link?

Ch: Yes but not common across borwsers

Some users like direct action, other sprefer to know what will happen before they allow it to.

Ch: Shipping browsers on Mac Ctrl-Alt is typical except Safari

DKA: What should the TAG do?

Ch: review the task force work

[discussion of addig extra key]

Ch: It is impossible to find key combos across all platfors

### CSS Regions Draft Feedback

[Special guest Alan Stearns joins for this part]

We are discussing CSS Regions, with Sergei’s review as a starting point

Peter: https://github.com/w3ctag/spec-reviews/blob/master/2015/01/CSS%20Regions.md

Alan: re Asking for use cases, I think Sergei is the only person I know who preferred the previous version of the spec, with more complex use cases.  
…The new spec is simpler — just “I want this content displayed over hre”  
…So each noe contributes to the design, but the content is bullt outward from the templatwe to the page  
…There is no way of having complex markup insered specifically into a design.  
…Grid layout will have slots, which are similar.  
…This is like slots without grids  
…Those are the use cases.

DKA: It is ok to push back on the review.

Alex: ANy complex layout system could require something like CSS regions

Alex: I have other concerns about regions. Extensibility - how to regions work?  
… This immplie stg about something whoch CSS has which has — this yet anothing which ives no way tto extract th ething into user space

Alex: Named flows do a verion of intrinsic width bawsed on container. You flow thinsg itno a contariner and wrap.

That is core to CSS, and ios not available to the rest of the system.

Remmeber IHT in 2002 doing pagination and layout? They all call out for the power

Peter: Fragmentation and line breaks are fifferent.

Alex: I am not opposed to having this in the platorm — but now in 2015 there are common features with things ike

Peter: Multicolumns etc

Alex: .. which are not available to the user.

Regions exposis more of the problem …

Alan: An early version of regions defined flow control myuch morepwoerfully but we pulled iot out as it was common to lot sof other things too

Alex: If youhave frag events, then there is some time, when we have promise delibvery etc etc end pof the layout cwork chunkc, time to move on.  
… This seems to be a well-constructed design. Just need these evnets

Alan: People have used named flows on singel box content.  
…There is a processing mosel fro dustribimg content amobne the boxes in the region chain

[discussion of detains of event timing sequence]

Alex: If we could alllow the app to fdo more work to particiapet in the layout process, that woul dbe useful

Alan: HArd to find exactly the right time to fire the event.

Alex: Why? You start with content and width constraints, you will end up with resolved widgth and height (in most cases) and hopeful you won’t cycle around.

Mike: -> http://dev.w3.org/csswg/css-break-3/ "Breaking the Web, one fragment at a time"

timbl has joined #tagmem

Peter: On another topic, event propogation.

… When something has flowed into a different box assocaited woth a diff som, where does the event go?

Travis: I hope - go withoriginal dom

Alan: Yes.

You will get the whole stack of things underneath it, and when that is available, then you wil be able to make it so events follow the stack not the original DOM tree.

Alex: So is A flows into B does the shadow dom from b get replaced with hat iof A?

Peter: Never change the DOM!

Alex: What is node.children for something which has been reflowed?

Alan: the original children

Alex: If I mutate the dom children, then they are out of the render tree?

Alan: yes

Alex: Looks like shadow root reoplacement

Peter: Kinda

Peter: If a dom noed os flowed into , ts chldren do not generate boxes

Alan: If you hav a flow from an alement with its own children, it stays its own regular self.

Alan: No Imeant [missed]  
…we didn't want a property that had an affect sometimes but not others  
…if you use flow-from on an element and there is no named flow, the element's children are not visually formatted  
…and if you use flow-into and there is no region chain, the named flow also does not display

Alex: before and after pseudo-elemnts — do the come from name flow?

Alan: No from region cchain

Alex: Thee apre populatde by aselector from the dom region

Alan .. whatver is craeting the box

Travis: An element A that adds a flow to (or a flow-from) stops rendering it's 'natural' children. (stops generating boxes)

Travis: It's only when the flow-from matches the flow-to that CSS Regions magic happens.

Alan: I f named flow content has before and after psedoelemnet,s they flow along the region change with everything else

peter: can we use flow from with before and after?

[Agreed: Too scary]

Alwx: You only use same-orogin IFrames here?

Travis: YEs, or you are pulling conetnt from one origi to annother.

Alan: The region spec has the content keyworkd for this iframe.

Alan: Ther is a way in CSS to sy “don’t display this parent box, but jsut ignoreit and display all its children”

http://drafts.csswg.org/css-display/#the-display-outside

Alan: Imlemented in Fiefox and Chrome maybe.

[Enter Brendan Eich stage right to general acclamation]

[discussion]

[Exit stage right chased by a bear]

Alex: I want to see example code of people useing CSS regions

Alan: The overwhelming use case is to add more dom nodes to cope with the overflow. Which a lot of people in the CSS WG reckon is bad bad  
…You make a region chain you think will hold will the stuff and then you add more boxes if yoiu were worng  
…Much quciker in fact to pare off unneeded extras than to add moer boxes.

ACTION: Travis to write some feedback on the work of the html accessibility task force work on focus navigation and activation…

Mark: have we moved on from a keyboard and a screen? What is the abstraction?

When you mutate the DOM as a result of layout, it can be horribly inefficient. Iwont the ability to be able to have two different views — layouts — of the same dm tree in principle

Alan: We ahd to allow people to make boxes with divs to be pragmatic - no other way

Peter: Boxes should be long term generated from the DOM tree, or declared in templates

Alan: Flow into anything which has a selector

DKA: Does this mean we can move on from regions — we have had sufficuent discussion

Alex: I think we can say we are excited about a box-tree based future  
…Need more work for users to be accss this but that should not block this work.

RESOLVED: close the review issue

[Exit Alan Stearns]

### Captive Portals

https://github.com/httpwg/wiki/wiki/Captive-Portals

Mark: The IETF recongize this as a major problem.  
…There is a DHCP option to indicate where you need t log into a captive portal. The orginal discussions had not onvolved the operators. The  
…soluion was actually godo but insuficiently discussed around  
…So we had a great discuss of all of this  
…Hotspot 2.0 is a new wifi roaming alloiance spec — we discussed  
…This if for when a huge movile business gets its phones to auto login to a set of wifi suppliers, like att wifi on apple.  
…A lot of places in fact nowadays are dropping the captive portal and just usig WEP security and a password.  
…There will porbably be a working group around captive portals — it will be important to get the operators to come and be invoolved.

DKA: There is an arms race bwteeen the captove portal people trying to catpture people baut the apple-like software trying to automate the process or put it itno a specially constraine bowser context

[discussion of advertizing based business models etc]

Tim: Why do CPs bitehr intercepting and rerouting HTTS connections anyway?

Peter: They want to be able to show you soemthing even if you strat looking for https: somehting

Mark: We need to tell people who want to do the right thing — like a home or a university — how to do the right thing.

Peter: And we need to alos talk about what haooens with th old providers who are not

[We Adjoun for the day.]

DKA: resolved: 🍺
