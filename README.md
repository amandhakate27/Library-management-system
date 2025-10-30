# Library-management-system

This is a Library Management API Backend for the management of users and the books 

# Routes  and the Endpoints


## /user 
GET : Get the list of all users in the system.
POST : Create/Register a new user

## /users/{id}
GET : Get a user by their ID
PUT : Updating a user by their ID
DELETE : Deleting a user by their ID (check if the user still has an issued book) && (is there any fine/penalty to be collected)


## /users/subscription-details/{id}
GET : Get a user subscription details by their ID
        >> Data of subscription
        >> Valid till ?
        >> Fine if any ?

## /books 
GET : Get all the books in the system
POST : Add a new book to the system

## /books/{id}
GET : Get a book by its ID
PUT : Update a book by its ID
DELETE : Delete a book by its ID

## /books/issued
GET : Get all the issued books

## /books/issued/withFine
GET : Get all issued books with their fine amount

### Subscription
    >> Basic (3 months)
    >> Standard (6 months)
    >> Premium (12 months)


>> if a user missed the renewal date, then user should be collected with $100
>> if a user missed his subscription, then user is expected to pay $100
>> if a user missed both renewal and subscription, then the collected amount should be $200.


## Command: 
npm init
npm i express -- save-dev

npm run dev

