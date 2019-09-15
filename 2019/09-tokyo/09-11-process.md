
## Process Discussion at Tokyo F2F (11 Sep 2019)

#### Flow of how an issue is created

* What is the role of the TAG?
  * How do we communicate to our "customers" what the role of the TAG is?

* What is a candidate for TAG review?
  * templates (API design, dispute resolution)
  * what is the "right size" for TAG review?
  * what is in/out of scope?
  
* What work items do we have that are not reviews?
  * Findings - short, sharp statements, saying something sage
  * Documents like the design principles and security & privacy self-check - things that we know and that we are constantly trying to explain, put together in themes - things that we expect spec authorts to have read before requesting TAG review.
  * Blog posts - usually used as a way to less formally anounce somehting else, but sometimes used to make a consensus statement (e.g. EME security researchers statement)
    
  * W3C Notes - Publishing & linking on the web - as a mechanism to get something in TR space
  * Meta: How do we manage issues that are not in our design reviews repo?


* What are the phases of a TAG review?

  Labels: https://github.com/w3ctag/design-reviews/labels


  * Progress - untriaged

     (Issue is assigned to TAG member(s) -> transition to Unreviewed)   BOT

  * Unreviewed
  
    (Comment added by any assigned TAG member -> transition to In Progress   BOT
 
  * In progress -- we'll change this to "Pending TAG action"
  
    FORMER DEFINITION (This means that the issue is still alive. For example, the meeting timed out before we finished the discussion, or one of us is going to do external research or discussion, etc. This can happen in parallel with a lot of other labels, below.)
    
    NEW DEFINITION (This means that we need to do something now. This should appear after external feedback has appeared, etc.)
 
  * Pending external feedback
 
  This is when we have asked for more information from the working group, and they haven't replied yet. 
  
  This is hard to code for... the bot won't know which comment comes from the external feedback that we were looking for.  The bot could be confused by comments from someone else.
  
  Maybe that's okay? We'll then need a human to look at the comment and decide if it's useful. 
 
  * Pending editor feedback
 
  * Pending transfer
 
  * Stalled
 
  * External help requested
  
  This is when we've asked for help from another expert, for example a former TAG member or an IETF IAB member. 
 
  * Breakout
 
  * Joint meeting
 
  * Proposed closing
 
  * Review complete
 


  * what are the triggers for changing phases?
  * what happens if our feedback is "Not LGTM"?
  * what resolutions are possible?
  * how do we manage issues that are controversial?
  * how do we manage issues where we don't have TAG consensus? 

* How does the TAG ensure we progress on issues in a timely manner (no "process starvation")?

* How do we avoid "the Abyss"?

* what is an Explainer for? Why do we require it?
  * alice to adopt some text to a start of a document on this
