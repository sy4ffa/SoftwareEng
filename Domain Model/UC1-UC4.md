## 1. UC-1(Register)

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Form specifying the fill parameters for database storage | K | Fill page
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Information regarding actor's account | K | Investigation requests
Filtered actor's infomration so every information entered correctly | D | Filterer
Prepare a database storage for storing actor's data | D | Database connection
Notified actor current status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Filterer | Controller passes the information of the form to Filterer | conveys requests
Filterer <-> Investigation requests | Filter all the information to confirm all the information follws the correct rule | generates
Filterer <-> Database Connection | Information filtered saved to database | requests save
Filterer <-> Notifier | Filterer request Notifier to notify actor regarding status of account | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | fill parameters | needed for actor to fill in sign up form, needed to filter new information written 
Investigation Requests | actor's information | actor's information needs to be investigate before confirming their account
Filterer | filter form | filter all the information filled to match the website rules
Notifier | notify actor | notify actor whether their signing up process a success or failure 

