# Simulator Cinema Service
#### This is a RESTful application that supports registration, authentication, authorization and CRUD operations, based on SOLID principles.
## Description
This is the simplest emulator of the program for cinemas - designed for the organization of cinemas and supports all the most necessary functions

Functions included in the program
Registration of new users
Login for registered users
Add and remove movies, screenings, and theaters
Add tickets to the cart and make an order

The program is divided into user and administrator access.
The user has the opportunity to view sessions, movies, manage their orders.
Admin can add or remove movies, sessions, etc.

Information is sent and received in JSON format.

## Features
- register or login user
- get and add movies
- get and add cinema halls 
- get, add and delete movie sessions 
- find users by email
- get movie sessions 
- create shopping card
- add tickets to shopping card 
- complete orders

## Available urls with Role
- POST: /register (All) - register new user
- GET: /cinema-halls (Admin/User) - get cinema halls
- GET: /movies (Admin/User) - get cinema movies 
- GET: /movie-sessions/available (Admin/User) - get available movie sessions
- POST: /cinema-halls (Admin) - create cinema halls
- POST: /movies (Admin) - create movies
- POST: /movie-sessions (Admin) - create movie sessions
- PUT: /movie-sessions/{id} (Admin) - update movie sessions by id
- DELETE: movie-sessions/{id} (Admin) - delete movie sessions by id
- GET: /users/by-email (Admin) - get user by email 
- GET: /orders (User) - get orders
- POST: /orders/complete (User) - create order
- PUT: /shopping-carts/movie-sessions (User) - add movie-sessions to shopping cart
- GET: /shopping-carts/by-user (User) - get shopping cart by user

## Technologies
- Java 11
- Spring 5.3.20 
- Spring Security 5.6.10 
- Hibernate 5.6.14.Final 
- Maven 
- MySQL 8.0.22 
- Tomcat 9.0.68

## How to run
- Clone the project from GitHub 
- Configure /resources/db.properties with your own URL, username, password and JDBC driver 
- Configure Tomcat server (it is recommended to use version 9.0.68)
- First user with the role of ADMIN will be created automatically with the following parameters: email - admin@i.ua, password - admin123
- First user with the role of USER will be created automatically with the following parameters: email - user@i.ua, password - user123
- Run and enjoy the program

## UML diagram
![](uml.png)