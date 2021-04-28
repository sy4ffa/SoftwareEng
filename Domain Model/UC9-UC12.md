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
Controller <-> Checker | Controller passes check request to Checker to make sure actor is in log in status | conveys requests
Database connection <-> Checker | Database passes the log in status to CHecker | provides data
Checker <-> Investigation requests | Making sure no abnormal actions that have not been accomplished | request check 
Checker <-> Notifier | Checker request Notifier to notify actor regarding actor's current status | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Checker | actor's status | check actor's status by making sure actor is in log in state 
Investigation Requests | hold activites | making sure there are no hold activities that have not been accomplished
Notifier | notify actor | notify actor whether logging out process is a success or not 

### Domain Model 

![image](https://user-images.githubusercontent.com/81685914/116350114-58fdfd80-a82c-11eb-9780-b58c4a676ce5.png)

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
Controller <-> Modifier | Controller passes the modify requests to Modifier | conveys requests
Database connection <-> Modifier | Database passes the products data to Modifier to modify products | provides data
Modifier <-> Filterer | Filter all the information to ensure no double saving the same products | request filter
Filterer <-> Database Connection | Information filtered saved to database | requests save
Filterer <-> Notifier | Filterer request Notifier to notify actor regarding status of account | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | edit parameter | needed for actor to edit any products wanted or adding a new product
Modifier | modify products | used to modify any products or adding/removing products
Filterer | filter products | filter modified products to avoid double saving the same product
Notifier | notify actor | notify actor whether their editting process has been saved or not

### Domain Model 

![image](https://user-images.githubusercontent.com/81685914/116350405-d9246300-a82c-11eb-8e1f-076585fbd1e2.png)

## _🍓UC-11 (Manage order)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Information regarding all the list of customer's order | K | Key
Able to check off any order that has been prepared | D | Checker
Prepare a database storage for storing recent managed products | D | Database connection
Notified actor which product needs to be manage next | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Checker | Controller passes check request to Checker | convey requests
Database connection <-> Checker | Database passes the data for order list to Checker | provides data
Checker <-> Notifier | Checker request Notifier to notify actor regarding which products have not been managed | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Checker | check off list | check off th eproducts from the list if the product has been prepared and ready for delivery 
Notifier | notify actor | notify actor which product to prepare for next

### Domain Model

![image](https://user-images.githubusercontent.com/81685914/116350669-4afcac80-a82d-11eb-94e1-ca787953e50d.png)

## _🍓UC-12 (Edit Status)_

Responsibility Description | Type | Concept Name
-------------------------- | ---- | ------------
Coordinate actions of concepts associated with this use case and delegate the work to other concepts. | D | Controller
Render the retrieved records into an HTML document for sending to actor's Web browser for display | D | Page maker
Information regarding order status | K | Key 
Form specifying the edit parameters for database storage | K | Edit page
HTML documentation that shows the actor the current context, what actions can be done, and outcomes of the previous actions | K | Interface Page
Change the order status to next level | D | Modifier
Prepare a database storage for storing recent order status data | D | Database connection
Notified actor current status | D | Notifier

Concept Pair | Association Description | Association Name
------------ | ----------------------- | ----------------
Controller <-> Page Maker | Controller passes request to Page Maker and receivers back pages prepared for displaying | conveys requests
Page Maker <-> Database Connection | Database Connection passes the retrieved data to Page Maker to render them for display | provides data
Page Maker <-> Interface Page | Page Maker prepares the Interface Page | prepares
Controller <-> Modifier | Controller passes modify request to Modifier | cnoveys requests
Database connection <-> Modifier | Database passes the order status to Modifier to modify order status | provides data
Modifier <-> Notifier | Modifier request Notifier to notify actor for his/her order status | requests notify 

Concept | Attributes | Attribute Description 
------- | ---------- | ---------------------
Page Maker | edit parameters | needed for actor to edit in the order status 
Modifier | modify status | modify current status of order
Notifier | notify actor | notify actor regarding current order status 

### Domain Model 

![image](https://user-images.githubusercontent.com/81685914/116350817-8a2afd80-a82d-11eb-924e-6a4411fbaa7f.png)
