#TAG Teleconference March 19, 2015

##Topic : CSS Regions Draft Feedback & IETF Miscellany

## Agenda: https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/03-19-cssregions.md

Chair: Dan  
Scribe: yan  
Present: Dan, Peter, Yan, Mark, Sergey, Yves, Travis, Alex, Tim  

http://dev.w3.org/csswg/css-regions-1/

dan: welcome. we're going to discuss css regions draft today and the permissions API review.

sergey: [introduces draft]. Currently does not align well with extensible web. Would be better explained using Houdini. They introduced a superset of DOM elements called [named flow?].

peter: editors are involved in houdini effort already. I agree with all the feedback.

sergey: There are two problems. It's not polyfillable and introduced high level APIs instead of low 

Travis: IE feels very good about the way regions are today.

sergey: This spec solves the problem they're trying to solve. But in terms of extensibility, it's introducing new magic instead of primitives.

Alex: I'd like to agree with sergey on couple of points. NOt concerned about polyfillability; lots of new things in the platform can't be polyfilled easily (like SW). Regions is about something that is expensive to polyfill. Indicates an area to focus questions. I'm more concerned about how flow works, and how you can't efficiently be part of some of it. There's no point in which I can say, "What event can i use to understand when overflow is computed?" There's nothing in the object model that lets us understand what [??] child is. Also I'd like to understand how regions can be implemented in a houdini world, would be a nice target for Houdini to satisfy.

sergey: should definitely specify box trees.

alex: box tree doesn't get us line break or text run stuff, i think?

peter: i don't think it would get you the writeable box tree, either.

Peter: writeable box tree isn't likely to happen

alex: that indicates we're missing a hook somewhere. Particularly when you've done a single layout and want to change the text runs so that you can take the rest and put it somewhere else.

sergey: CSS Regions define superset of DOM elements; to avoid that you need certain primitives.

alex: is there a proposal in houdini to identify result of a flow [??] transposition of content fragment.

peter: houdini effort will create a hook to emulate css region. so i think this will be explainable from the houdini effort with the current hooks. sergey's other point is that the regions spec creates extra boxes for content to flow into, many people are complaining about that in CSSWG. Shouldn't create DOM struction for layout purposes.

sergey: [??] instead of normal semantic HTML, which isn't desirable. You may specify CSS regions in semantic way but people probably won't.

peter: Also can't declaratively create extra boxes. You should be able to participate in region flow without touching the DOM.

dka: action proposal. People are generally happy with the doc, but there are specific objections that alex has voiced and in IRC log. Can you take the action of adding these items to the current draft? We can then declare it done and then push to the relevant people, like Houdini.

[Proposed way forward: Someone [alex?] takes on the roll of fleshing out the current draft to reflect this discussion and then we push this to the group and also make it an input to Houdini.]

alex: my major feedback is that it looks like houdini is already on it. Primary feedback is that polyfilling regions efficiely should be part of those deliverables . I don't think we have feedback other than "go houdini!"

Peter: I don't think any of this is new to the working group. But TAG should say what issues are important and give their feedback.

dka: In that case, should we add anything to feedback or just fire it off to the relevant people?

alex: I think we should edit what's there now, rephrase in terms of Houdini as a challenge to Houdini.

dka: Assigned to Alex. [https://github.com/w3ctag/spec-reviews/issues/47]

timbl: here we are building something that has an API at every level, every piece can be re-implemented and replaced. That's a great model for extensibility it seems but actually it completely prevents [??] because you'll never be able to change how CSS works altogether once you expose boxes.

alex: this comes up frequently. I think ppl on browser engines need to get used to this. Supporting backwards compatibility doesn't necessarily preclude anything. We only "go slow" for old features that we wish people wouldn't be using, otherwise we can go fast.

Peter: We're exposing events that people can hook into, but we're not setting the details of the layout (like boxes) in stone. That happens in the browser under the hood.

dka: let's transition to the permissions draft review. mark, do you want to talk about IETF?

mark: i probably want to do that after the IETF meeting next week. a lot is going on. not sure if i can be in the call next week.

peter: [offers to coordinate]

dka: i suggest we hold the call next week and focus on agenda planning for april - https://github.com/w3ctag/meetings/blob/gh-pages/2015/04-sfo/agenda.md   

[discussion of meeting time in the future. consensus that 1 hour later is ok?]
https://github.com/w3ctag/spec-reviews/blob/master/2015/01/CSS%20Regions.md

alex: there's an early draft of permissions API spec review. please look at it. i'm continuing to update the document, probably in time for next week's call.

travis: i read it with some folks, we had comments. i'll try to get them in.

mark: are you going to discuss logistics for april if i'm not here?

dka: yes, put items in agenda/wiki (agenda link above). Please all come to the extensible web summit. I sent out an eventbrite link. Tantek probably speaking at a lightning talk. Also we launched https on extensible web summit website!

mark: are we doing meet the tag event?

dka: no, since the extensible web summit covers it.

mark: my only concern is the name is too restrictive.  

dka: can't change it, but could use help with messaging. reach out to developers who should come and re-state that this is not just about the extensible web, it's about the web platform. happy to rename, we can talk about that. or we could fork the event.  

https://extensiblewebsummit.org  

From IRC:  
slightlyoff: I'm not sure a lack of polyfillability should be a big ding; lots of new capabilities can't be (e.g., SWs)  
[7:17pm] slightlyoff: but I agree about the lack of explanation  
[7:17pm] slightlyoff: so I'm concerned that we don't have:  
[7:17pm] slightlyoff: 1.) line breaking primitives  
[7:17pm] slightlyoff: 2.) the ability to participate in layout deeply enough to use those line breaks to handle it  
[7:18pm] slightlyoff: 3.) a new content addressing mechanism  
[7:18pm] slightlyoff: 4.) no ability to hook CSS parsing (fixed by houdini?)  

Also to add to the agenda (from Alex): https://github.com/w3ctag/spec-reviews/blob/master/2015/03/Permissions.md




