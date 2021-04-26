## _🍓UC-1(Register)_

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
Filterer <-> Investigation requests | Filter all the information to confirm all the information follows the correct rule | generates
Filterer <-> Database Connection | Information filtered saved to database | requests save
Filterer <-> Notifier | Filterer request Notifier to notify actor regarding status of account | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | fill parameters | needed for actor to fill in sign up form, needed to filter new information written 
Investigation Requests | actor's information | actor's information needs to be investigate before confirming their account
Filterer | filter form | filter all the information filled to match the website rules
Notifier | notify actor | notify actor whether their signing up process a success or failure 

## _🍓UC-2(Log In)_ 

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Form specifying the fill parameters for database storage | K | Fill page
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Information regarding actor's account | K | Investigation requests
Filtered actor's infomration so ID and password entered correctly | D | Filterer
Retrieve data from database and compare with actor's information | D | Database Connection
Notified actor current status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Database Connection | Controller passes the request to retrieve data regaring actor's log in information | conveys requests
Controller <-> Filterer | Controller passes the information of the form to Filterer | conveys requests
Filterer <-> Investigation requests | Filter all the information to confirm email/ID and password are matched | generates 
Filterer <-> Notifier | Filterer request Notifier to notify actor regarding status of log in | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | fill parameters | needed for actor to log in, needed to filter email/ID and password written 
Investigation Requests | actor's information | actor's information needs to be investigate wiht previous data stored
Filterer | filter form | filter all the information filled 
Notifier | notify actor | notify actor whether their logging in process a success or failure 

## _🍓UC-3(Fill Info)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Check whether actor is in log in state or not | D | Investigation requests
Form specifying the fill parameters for database storage | K | Fill page
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Information regarding actor's payment and address details | K | Investigation requests
Filtered actor's infomration to ensure all information entered correctly | D | Filterer
Prepare a database storage for storing actor's data | D | Database connection
Notified actor current status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Controller <-> Interface page | Controller passes the request to ensure actor is in log in state or not | conveys requests
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Filterer | Controller passes the information of the form to Filterer | conveys requests
Filterer <-> Investigation requests | Filter all the information to confirm all the information follows the correct rule | generates
Filterer <-> Database Connection | Information filtered saved to database | requests save
Filterer <-> Notifier | Filterer request Notifier to notify actor regarding status of account | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | fill parameters | needed for actor to fill in payment and address details, needed to filter new information written 
Investigation Requests | actor's information | actor's information needs to be investigate before confirming their details
Filterer | filter form | filter all the information filled to ensure the card and house address exists
Notifier | notify actor | notify actor whether their details is correct or not

## _🍓UC-4(See Products)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Information regarding website | K | Investigation requests

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | website parameters | displays products and information allowed to actors
Investigation Requests | website's information | shows websites information 




