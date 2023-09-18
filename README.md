# Al-Akeel-Food-Ordering
Tools Project - Al Akeel Food Ordering Platform

Sorry for the lately Note but here are the authorization data in order to access the api's :

Customer 
username: customer
password: customer1!

RestuarantOwner
username: owner
password: owner12!

Runner
username: runner
password: runner1!


# Al-Akeel Food Ordering Platform

## Introduction

Al-Akeel Company has developed an online order management platform over the past 15 Years. This platform allows users to make online orders to a specific restaurant from a registered restaurant list. It also tracks and delivers such orders from the restaurant's locations to the customer. The platform serves clients from either a dedicated mobile application, web app, or assisted from customer service over the phone. The platform allows restaurant staff to manage their restaurant-specific orders. The platform integrates with Bank Misr as a payment gateway to fulfill online payments for orders. The platform integrates with Aramex shipment company to manage the delivery of orders. Recently, the company started to face a set of issues, mainly reliability issues where sometimes the platform reported to be down. It suffers from slow responses. They also faced a huge challenge when they needed to support mobile payment as well as support Al-Akeel specific shipment fleet to work side by side with the existing Aramex shipment.

## Entities

- **User**: Id, name, role
- **Meal**: id, name, price, fk_restaurantId
- **Order**: Id, Item array, total_price, fk_runnerId, fk_restaurantId, order_status (preparing, delivered, canceled)
- **Runner**: Id, name, status (available, busy), delivery_fees
- **Restaurant**: Id, name, ownerId, list of meals

**Note:** Add any additional fields if needed.

## System Functionalities

### User Roles: Customer, RestaurantOwner, Runner

#### Restaurant Owner
- Sign up and Login
- Create restaurant menu
- Edit restaurant (change menu meals for each restaurant)
- Get restaurant details by id
- Create restaurant report: Given a restaurant id, print how much the restaurant earns (summation of the total amount of all completed orders), Number of completed orders, Number of canceled orders

#### Customer
- Sign up and Login
- Create order by customer
  - Expectations: imagine a normal restaurant receipt. Order details should contain date, restaurant name, items list, delivery fees, runner name, total receipt value (summation of items prices, delivery fees)
- List orders by customer id
- When creating an order, select a random available runner from the database and assign it to an order and convert his status to busy
- Edit order [change an order’s items]: Make sure an order is not canceled and it is in the preparing state to be edited
- List all restaurants

#### Runner
- Sign up and Login
- Mark an order as delivered and change his status to available
- Get the number of trips completed by a runner: Make sure orders are not canceled and marked as completed

## Project Guidelines

- You can use any relational database, you can use an in-memory database (Recommended DB: SQLite)
- You must use GIT for source code management and create a private repository on GitHub
  - Add your TA to git repo:
    - Eng Esraa: e.salem@fci-cu.edu.eg
    - Eng Mohamed: m.samir@fci-cu.edu.eg
    - Eng Mahmoud: m.hadad@fci-cu.edu.eg
- Teams should be of 3 - 4 members 
- Create a Postman collection containing the created APIs to be used in the discussions

## Bonus Tasks

- Create a Frontend Application using any JavaScript Framework (Angular, React, VueJS) including the GUI of all the requested functionalities (+2 Marks)
