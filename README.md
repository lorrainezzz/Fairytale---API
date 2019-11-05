# Assignment 1 - Agile Software Practice.
My name is Yang Zou. And student id is 20086439.

## Overview.

This web app is for users to search fairy tale and read. And there will be an admin. He can add new fairy tales or authors, and he can delete the fairy tale or author.

## API endpoints.

 User
 
 + GET /user - Get all users.
 + GET /user/:id - Get a user with a particular id.
 + POST /user/register - User can register with a new account and update the new account infomation to the database.
 + POST /user/login - User can login with the exist account in the database.
 
 Admin
 
 + GET /admin - Get all admins.
 + GET /admin/:id - Get an admin with a particular id.
 + POST /admin/register - Admin can register with a new account and update the new account infomation to the database.
 + POST /admin/login - Admin can login with the exist account in the database.
 
 Fairy Tale
 
 + GET /fairytale - Get all fairy tales.
 + GET /fairytale/:id - Get a fairy tale with a particular id.
 + POST /fairytale - A new fairy tale can be added into the database and update the database.
 + DELETE /fairytale/:id - A fairy tale can be deleted with a particular id. Then, update the database.
 
 Author
 
 + GET /author - Get all authors.
 + GET /author/:id - Get an author with a particular id.
 + POST /author - A new auhtor can be added into the database and update the database.
 + DELETE /author/:id - An author can be deleted with a particular id. Then, update the database.
 

## Data model.


![image](https://github.com/lorrainezzz/Fairytale---API/blob/master/structure.jpg)


## Sample Test execution.

~~~
Admin
    GET /admin
      √ should GET all the admins (47ms)
    GET /admin/:id
      when the id is valid
        √ should return the matching admin
    POST /admin/register
      √ should return name can not be empty message (38ms)
      √ should return password can not be empty message
      √ should return name occupied message
      √ should return confirmation message and update mongodb
    POST /admin/login
      √ should return name or password can not be empty message
      √ should return name is not exist message
      √ should return wrong password message
      √ should return confirmation message and update mongodb

  10 passing (6s)
~~~
~~~
  Author
    GET /author
      √ should GET all the authors (80ms)
    GET /author/:id
      when the id is valid
        √ should return the matching author
    POST /author
      √ should return can not be empty message (43ms)
      √ should return author already existed message
      √ should return confirmation message and update mongodb
    DELETE /author/:id
      when the id is valid
        √ should return confirmation message and update database
      when the id is invalid
        √ should return the NOT found message
   7 passing (6s)s
~~~
~~~
User
    GET /user
      √ should GET all users (48ms)
    GET /user/:id
      when the id is valid
        √ should return the matching user
    POST /user/register
      √ should return username can not be empty message
      √ should return password can not be empty message
      √ should return name is existed message
      √ should return confirmation message and update mongodb
    POST /user/login
      √ should return username or password can not be empty message
      √ should return username is not exist message
      √ should return wrong password message
      √ should return confirmation message and update mongodb
  10 passing (5s)

~~~
~~~
 Fairytale
    Fairy tale
      GET /fairytale
        √ should GET all fairy tales (49ms)
      POST /fairytale
        √ should return name or author cannot be empty message
        √ should return fairy tale has already existed message
        √ should return confirmation message and update mongodb
      DELETE /fairytale/:id
        when the id is valid
          √ should return confirmation message and update database
        when the id is invalid
          √ should return the NOT found message
  6 passing (6s)

~~~



