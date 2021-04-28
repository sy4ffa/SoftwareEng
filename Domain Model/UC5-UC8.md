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
Controller <-> Storer | Controller passes a list of products available in the Cart to the Storer | convey requests
Storer <-> Filterer | List of products in the Cart being filtered to ensure the products is available | provides data
Storer <-> Database Connection | Products in the cart is saved to database | requests save
Storer <-> Notifier | Storer request Notifier to notify actor regarding status of cart | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | button parameters | needed for actor to add in products to the cart 
Storer | Cart Storage | products stored in the cart is final and saved to database after being filtered 
Filterer | filter cart | filter all the products in the cart to ensure its availability
Notifier | notify actor | notify actor whether their adding to cart process is a success or failure 

### Domain Model 

![image](https://user-images.githubusercontent.com/81685914/116348720-92813980-a829-11eb-9102-16431544d00a.png)

## _🍓UC-6 (To Pay)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Checking whether there are any card details added for payment or not | D | Seeker
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
Controller <-> Seeker | Controller passes card details of the User to check whether there are any card added or not in the account for payment purposes | convey requests
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Seeker <-> Filterer | Seeker convey the payment details to Filterer | filter
Filterer <-> Investigation requests | Filter all the information to confirm all the details is correct | generates
Filterer <-> Database Connection | Information filtered saved to database | requests save
Filterer <-> Processor | Filtered card details being used to process payment | generates 
Processor <-> Notifier | Processor request Notifier to notify actor regarding status of payment | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Seeker | search card | to search whether there are any card registered 
Page Maker | fill parameters | needed for actor to fill in payment details if no card is being registered yet
Filterer | filter card | filter all the card information to ensure the validity of the card
Processor | process payment | process payment regaring the products bought 
Notifier | notify actor | notify actor whether their payment process is a success or a failure 

### Domain Model

![image](https://user-images.githubusercontent.com/81685914/116349245-8ba6f680-a82a-11eb-91e6-a014c27829fc.png)

## _🍓UC-7 (Get Email)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Check whether an email is available in th eactor's account | D | Seeker
Information regarding actor's email | K | Key
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Filtered actor's email to check its validity | D | Filterer
Send email confirmation regarding products ordered | D | Processor 
Notified actor email status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Seeker | Controller passes request to Seeker | convey requests
Database Connection <-> Seeker | Database connection passes the information of email address to Seeker | provides data
Seeker <-> Filterer | Seeker passes the email address to Filterer to check validity | generates
Filterer <-> Processor | Filter conveys the email address to Processor for further processing | request send
Processor <-> Notifier | Processor request Notifier to notify actor regarding status of order | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Seeker | email address | search if there are email provided by actor in the account 
Filterer | filter email | filter email to ensure validity
Processor | send email | send email to the email address provided to update regarding order status
Notifier | notify actor | notify actor whether their email has been sent or not 

### Domain Model 

![image](https://user-images.githubusercontent.com/81685914/116349492-1687f100-a82b-11eb-86c3-f4c4714ae973.png)

## _🍓UC-8 (See Order Status)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Check the actor log in status | D | Checker 
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Information regarding actor's account | K | Key
Retrieve data regarding actor's order | D | Database connection
Container for actor's order list | K | Key Storage
refresh and update actor's latest order status | D | Updater
Notified actor current order status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Checker | Controller passes request to Checker to check actor's log in status | conveys requests
Checker <-> Database connection | Checker retrieve data from database to check actor's status | retrieve data
Checker <-> Updater | Checker request to Updater to update recent order status of actor | request update
Updater <-> Notifier | Updater request Notifier to notify actor regarding status of order | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Checker | actor's status | check actor's status before giving in any information 
Updater | update order status | update order status of actor to the recent one 
Notifier | notify actor | notify actor regarding their order status 

### Domain Model

![image](https://user-images.githubusercontent.com/81685914/116349690-84341d00-a82b-11eb-9d0b-0e0137d0f770.png)

