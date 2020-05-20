# Getting To Done

The OCDS Definition Of Done has 5 requirements:

* Any issues or further work resulting from it is documented
* Any functionality changes are appropriately documented
* The code meets any applicable quality standards (tests, comments, etc)
* Any functionality changes either have been deployed/released, or a deploy/release has been scheduled 
* If appropriate, the solution has been approved by the original reporter / requester - especially if it's someone who works for ODSC or OCP

This how-to guide sets out common procedures and guidance for how to ensure that each of these 5 requirements are met. 

## Any issues or further work resulting from it is documented

It's very common for a piece of work to raise other issues, and for us to have ideas as to what to do next. To avoid scope creep, these should be documented, rather than assuming that they should be done immediately.  

* Any ideas for future improvements should be added as GitHub Issues in the relevant repo
* If you think that those ideas are important to do relatively soon, add Trello cards for each one, and start to draft a Definition Of Ready
* Bugs should be fixed as part of the work
* Unforeseen shortcomings are a judgement call; comment on the relevant GitHub issue and directly contact whoever is affected to ask

## Any functionality changes are appropriately documented

First, ascertain where the functionality is documented. This might include ReadTheDocs sites, OCP or ODSC-internal documentation, and code comments. 
Then, update to reflect any changes
Then, consider whether the person who asked for the work would have been able to find the functionality, if it had existed. For example, if the requester was following a procedure, has the procedure been amended?

## The code meets any applicable quality standards (tests, comments, etc)

In most cases, "applicable" means "in line with, or a slight improvement over, other parts of the code in the same repo". 

## Any functionality changes either have been deployed/released, or a deploy/release has been scheduled

If the functionality change is to a live web application, then it should either be accessible on the Web, or a date should be given for when the deploy will take place. If the change is to software that is downloaded by users, then it should have been released.

## If appropriate, the solution has been approved by the original reporter / requester - especially if it's someone who works for ODSC or OCP

"Approval" in this context is to say that the change that has been made meets the need that was set out to be met, and that everyone who needs to be aware of it, is. Sometimes that requires testing, and other times just acknowledgement of notification that a change has been made. 

Additional needs that emerge should be documented as additional GitHub Issues & Trello cards.

In order to seek approval from ODSC Analyst(s):
First, go to the OCP CRM and open a new ticket in the OCDS Technical Development project
Then, write the body of the ticket containing:
* A link to the relevant Trello card 
* A clear description of the change that has been made
* A summary of the testing that has been carried out so far
* A clear description of what you're asking for - prefer explicit questions to implicit requests
* Details of any deadlines, such as when you're planning to deploy
* Clear details of what will happen once approval is given
Then, assign the ticket to either the individual analyst who requested the change, or to Everyone (excluding non-OCDS ODS) group. If you want to ask a specific group of people, add them as Watchers.  
Then, update the Trello card with a link to the CRM ticket, and a summary of what's been asked for. 

Note that a new ticket should be opened for each change, even if you're opening several at once, so that each can be handled in its own way. 

### Example Ticket - Testing Required

Hi Michelle,

I've been working on the change to Kingfisher Views that you asked for in https://trello.com/c/EoAipkKH/999-make-views-awesomer . I've changed the Foo so that it Bars in the way that you asked for, and I've tested using the data that you supplied. 

Please can you test out the change in a local VM and see if it works for you with some other test data? Let me know if you need any help with a local VM; there's a HOWTO at http://example.com/kf-views-VM if you've not used it before. 

I'd like to deploy this before I move off OCDS at the end of next week, so if you could let me know by the 14th if you've either tested it, or won't get a chance to, I can respond appropriately. 

If it works for you, then I'll deploy it by the 17th at the latest. 

Thanks!

Abdul

### Example Ticket - Notification 

Hi Helpdesks! 

I've been working on the change to Kingfisher Views that you asked for in https://trello.com/c/EoAipkKH/999-make-views-awesomer . I've changed the Foo so that it Bars in the way that you asked for, and I've tested using the data that you
supplied. I've deployed the changes to live and updated the kf-views docs, so do try it out next time you're Bar-ing. 

Please can you reply to let me know once you've seen this and if any changes or other documentation is required? I'm on OCDS for the next few weeks, so there's no rush, but I'm obviously keen to get this finished. 

Kat
