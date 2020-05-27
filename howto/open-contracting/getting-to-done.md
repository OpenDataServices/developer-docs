# Getting To Done

The OCDS Definition Of Done has 5 requirements:

* Any issues or further work resulting from it is documented
* Any functionality changes are appropriately documented
* The code meets any applicable quality standards (tests, comments, etc)
* Any functionality changes either have been deployed/released, or a deploy/release has been scheduled 
* If appropriate, the solution has been approved by the original reporter / requester - especially if it's someone who works for ODSC or OCP

This how-to guide sets out common procedures and guidance for how to ensure that each of these 5 requirements are met. These procedures aren't mandatory, but rather embody some things we've learned and are a move towards a standard way of doing things, to avoid having to re-invent the wheel.  

## Any issues or further work resulting from it is documented

It's very common for a piece of work to raise other issues, and for us to have ideas as to what to do next. To avoid scope creep, these should be documented, rather than assuming that they should be done immediately.  

First, review your work to ascertain what changes have been made
Then, review any GitHub issues that you've already opened
Then, fix any issues that are clearly bugs
Then, ensure that GitHub issues have been raised for any issues that you're aware of, and that they stand as independent issues with sufficient detail for them to be left
Then, add GitHub issues for any further work that you think might be good to do
Then, add any ideas that you think are important to do soon to the Ideas & Reports column on Trello, with a draft Definition Of Ready
Finally, check the check-box on the Trello card that you're working on to confirm that you've done this

Notes:
* Unforeseen shortcomings are a judgement call; comment on the relevant GitHub issue and directly contact whoever is affected to ask

## Any functionality changes are appropriately documented

First, ascertain where the functionality is documented. This might include ReadTheDocs sites, OCP or ODSC-internal documentation, and code comments. 
Then, update to reflect any changes
Then, consider whether the person who asked for the work would have been able to find the functionality, if it had existed. For example, if the requester was following a procedure, has the procedure been amended?
Finally, check the check-box on the Trello card that you're working on to confirm that you've done this 

## The code meets any applicable quality standards (tests, comments, etc)

First, review other code in the same repo to ascertain conventions
Then, review documentation - such as the Standard Development Handbook, this developer documentation and the documentation for the repo you're working on to ascertain any further requirements 
Then, review your code to check that it's to the same standard, and update it if necessary
Finally, check the check-box on the Trello card that you're working on to confirm that you've done this

Notes:
* In most cases, "applicable" means "in line with, or a slight improvement over, other parts of the code in the same repo". 
* If the change you're making doesn't seem to need this, you can skip this step, and note that on the Trello card

## Any functionality changes either have been deployed/released, or a deploy/release has been scheduled

First, ascertain what "deployed" or "released" means for the code you're working on, and how to go about making that happen
Then, either:
* Schedule a release/deploy for a future date, and comment on the Trello card to say when it is
* Carry out a release/deploy
Finally, check the check-box on the Trello card that you're working on to confirm that you've done this

Notes:
* It's ok to deploy or release small changes; there's often limited benefit to bundling changes together

## If appropriate, the solution has been approved by the original reporter / requester - especially if it's someone who works for ODSC or OCP

"Approval" in this context is to say that the change that has been made meets the need that was set out to be met, and that everyone who needs to be aware of it, is. Sometimes that requires testing, and other times just acknowledgement of notification that a change has been made. 

Additional needs that emerge from the approval process should be documented as additional GitHub Issues & Trello cards.

In order to seek approval from ODSC Analyst(s):
First, go to the OCP CRM and open a new ticket in the OCDS Technical Development project
Then, write a title that will read well in an email notification, specifying which products have changed, introducing the change that's been made, and summarising the action (if any) required. 
Then, write the body of the ticket containing:
* A link to the relevant Trello card 
* A clear description of the change that has been made
* A summary of the testing that has been carried out so far
* A clear description of what you're asking for - prefer explicit questions to implicit requests
* Details of any deadlines, such as when you're planning to deploy
* Clear details of what will happen once approval is given
Then, assign the ticket to either the individual analyst who requested the change, or to Everyone (excluding non-OCDS ODS) group. If you want to ask a specific group of people, add them as Watchers.  
Then, update the Trello card with a link to the CRM ticket, and a summary of what's been asked for. 

Notes:
* In general, a new ticket should be opened for each change, even if you're opening several at once, so that each can be handled in its own way. 

### Example Ticket - Testing Required

#### Kingfisher Views: Foos now Bar - testing help please!
 
Hi Michelle,

I've been working on the change to Kingfisher Views that you asked for in https://trello.com/c/EoAipkKH/999-make-views-awesomer . I've changed the Foo so that it Bars in the way that you asked for, and I've tested using the data that you supplied. 

Please can you test out the change in a local VM and see if it works for you with some other test data? Let me know if you need any help with a local VM; there's a HOWTO at http://example.com/kf-views-VM if you've not used it before. 

I'd like to deploy this before I move off OCDS at the end of next week, so if you could let me know by the 14th if you've either tested it, or won't get a chance to, I can respond appropriately. 

If it works for you, then I'll deploy it by the 17th at the latest. 

Thanks!

Abdul

### Example Ticket - Notification 

#### Kingfisher Views: Foos now Bar - notification

Hi Helpdesks! 

I've been working on the change to Kingfisher Views that you asked for in https://trello.com/c/EoAipkKH/999-make-views-awesomer . I've changed the Foo so that it Bars in the way that you asked for, and I've tested using the data that you
supplied. I've deployed the changes to live and updated the kf-views docs, so do try it out next time you're Bar-ing. 

Please can you reply to let me know once you've seen this and if any changes or other documentation is required? I'm on OCDS for the next few weeks, so there's no rush, but I'm obviously keen to get this finished. 

Kat
