# Book-record-managemnet

This is a book record management API Backend for the management of records and books.

# Routes and Endpoints 

## /users
POST: Create a new user
GET: Get all list of users

## /users/{id}
GET: Get a user by id
PUT:Update a user by id
DELETE: Delete a user by id (check if he/she still has an issued book) (is there any fine to be paid)

## /user/subscription-details/{id}
GET: Get uder subscritption details
1. Date of subscrition
2. Valid till
3. Fine if any

## /books
GET: Get all books
POST: Create/Add a new book

## /books/{id}
GET: Get a book by id
POST: Update a book by id

## /books/issued/by-user
GET: Get all issued books

## /books/issued/withFine
GET: Get all isssued with fine

# Subscription types
Basic (3 months)
Standard (6 months)
Premium (12 months)


NOTE : DAtes will be in format mm/dd/yyyy


If the subscription date is 01/08/22
and subscription type is standard
the valid till date will be 01/02/23

If he has an issued book and the book is to be returned on 01/01/23
and he misses it, then he gets afine of rs.100

If he has an issued book and the issued book isto be returned at 01/01/23
If he misses the date of return , and his subs also expires, then he will get a fine of rs 200.

