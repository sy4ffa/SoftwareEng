## _🍓UC-5 (Add To Cart)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Button specifying the add funtion to the cart | K | Key 
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Container for the collection of products in the cart | K | Key Storage
Operate the products to be kept in the cart | D | Storer 
Filter the products in the Cart to ensure its availability | D | Filterer
Prepare a database storage for storing products in Cart | D | Database connection
Notified actor current cart status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Interface Page <-> Key | Interface Page shows the button display for adding item into cart | prepares
Controller <-> Storer | Controller passes a list of products available in the Cart to the Storer | convey requests
Controller <-> Filterer | Controller passes the list of products available in the Cart for filter purposes | conveys requests
Storer <-> Filterer | List of products in the Cart being filtered to ensure the products is available | Investigation requests
Storer <-> Database Connection | Products in the cart is saved to database | requests save
Storer <-> Notifier | Storer request Notifier to notify actor regarding status of cart | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | button parameters | needed for actor to add in products to the cart 
Storage | Key Storage | what type of products been saved to the cart 
Storer | Cart Storage | products stored in the cart is final and saved to database after being filtered 
Filterer | filter cart | filter all the products in the cart to ensure its availability
Notifier | notify actor | notify actor whether their adding to cart process is a success or failure 

## _🍓UC-6 (To Pay)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Checking whether there are any card details added for payment or not | D | Searcherer 
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Form specifying the fill parameters for database storage | K | Fill page
Information regarding actor's payment details | K | Key
Filtered actor's information so every information entered correctly | D | Filterer
Prepare a database storage for storing actor's payment data | D | Database connection
Payment being processed | D | Processor
Notified actor current status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Controller <-> Database Connection | Controller passes request to Database Connection to retrieve data regarding User's card details | conveys requests
Controller <-> Searcherer | Controller passes card details of the User to check whether there are any card added or not in the account for payment purposes | provides data 
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Filterer | Controller passes the payment details to Filterer | conveys requests
Filterer <-> Investigation requests | Filter all the information to confirm all the details is correct | generates
Filterer <-> Database Connection | Information filtered saved to database | requests save
Filterer <-> Processor | Filtered card details being used to process payment | generates 
Processor <-> Notifier | Processor request Notifier to notify actor regarding status of payment | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Searcherer | search card | to search whether there are any card registered 
Page Maker | fill parameters | needed for actor to fill in payment details if no card is being registered yet
Filterer | filter card | filter all the card information to ensure the validity of the card
Processor | process payment | process payment regaring the products bought 
Notifier | notify actor | notify actor whether their payment process is a success or a failure 

## _🍓UC-7 (Get Email)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Check whether an email is available in th eactor's account | D | Searcherer 
Information regarding actor's email | K | Key
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Filtered actor's email to check its validity | D | Filterer
Send email confirmation regarding products ordered | D | Sender 
Notified actor email status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Database Connection <-> Searcherer | Database connection passes the information of email address to Searcherer | provides data
Searcherer <-> Filterer | Searcherer passes the email address to Filterer to check validity | generates
Filterer <-> Sender | Filter conveys the email address to Sender for further processing | conveys send
Sender <-> Notifier | Sender request Notifier to notify actor regarding status of order | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Searcherer | email address | search if there are email provided by actor in the account 
Filterer | filter email | filter email to ensure validity
sender | send email | send email to the email address provided to update regarding order status
Notifier | notify actor | notify actor whether their email has been sent or not 

#3 _🍓UC-8 (See Order Status)_


