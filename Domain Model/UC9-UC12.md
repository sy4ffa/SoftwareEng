## _🍓UC-9(To Log Out)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Making sure actor is in log in status | D | Checker 
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Information regarding actor's account | K | Key 
Making sure there are no hanging actions that has not been done | D | Investigtion requests
Notified actor current status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Checker | Controller passes request to Checker to make sure actor is in log in status | conveys requests
Checker <-> Investigation requests | Making sure no abnormal actions that have not been accomplished | request check 
Checker <-> Notifier | Checker request Notifier to notify actor regarding actor's current status | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Checker | actor's status | check actor's status by making sure actor is in log in state 
Investigation Requests | hold activites | making sure there are no hold activities that have not been accomplished
Notifier | notify actor | notify actor whether logging out process is a success or not 

## _🍓UC-10 (Edit Products)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
List of products available | K | Key
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Container regarding the products available | K | Key Storage
Modify/add any products information | D | Modifier 
Filtering new data to avoid same data being saved double times | D | Filterer
Prepare a database storage for storing modifications added | D | Database connection
Notified actor current editting status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Modifier | Controller passes the information of the products to Modifier | provides data
Modifier <-> Filterer | Filter all the information to ensure no double saving the same products | request filter
Filterer <-> Database Connection | Information filtered saved to database | requests save
Filterer <-> Notifier | Filterer request Notifier to notify actor regarding status of account | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | edit parameter | needed for actor to edit any products wanted or adding a new product
Modifier | modify products | used to modify any products or adding/removing products
Filterer | filter products | filter modified products to avoid double saving the same product
Notifier | notify actor | notify actor whether their editting process has been saved or not 
