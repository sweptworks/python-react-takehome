# python-react-takehome
Swept coding take home challenge. This little project allows you to showcase your skills developing with our tech stack.

## Overview

Create a Python/Flask app (api only) that allows customers to create service requests from a react app. The features of the app include 

1. Customers can create service requests
2. Customers can search service requests by ID or date range 


### Functional Specification

1. No sign-in/sign-up/logout required 
2. Customers are identified only by their email addresses 
3. All services are predefined (pre-seeded in the DB) and customers can only choose from a dropdown
4. Work Orders cannot be scheduled in the past only in the future
5. All available time slots should be used. For example, if a service request is deleted, and a new one is created. The available slots should be used for the newly created requests
6. Durations should be in minutes. Example 25.1 would mean 25 minutes 6 seconds but should be presented to users after a search in a friendly format. For example, after a successful search, I wouldn't show 65.40 to a user rather 1hr 5min would be more appropriate. Please feel free to spell out the hours and minutes if you so desire. 
7. Work orders should not be created for the following 
    - Any date that is a holiday 
    - Sundays 
    - Anytime before 9 am and after 5 pm Monday - Saturday


### Customer Workflow (Create Service Request)

1. Enter email address 
2. Select Service from dropdown 
3. Clicks Create 

> Expectation: I should see the work order created for my service request

### Customer Workflow (Search Service Request By ID)

1. Enter a service request ID
2. Click Search or press Enter 

> Expectation: I should see the work order for the specific service request 

### Customer Workflow (Search Service Request By Date Range)

1. Enter a date range 
2. Click Search 

> Expectation: I should see all work orders for the service requests in that date range grouped by service request ID 


### Schema.sql 

```
Service 
    > ID
    > Name
    > Duration

WorkOrder
    > ID
    > ServiceID 
    > CustomerID 
    > EmployeeID

Holiday 
    - date 

TODO 
    > Create the entity for the work order relation
```

> Note: Feel free to add other columns to the above schema if you think they'd be useful. For example, you can add a `created_at` and `updated_at` for each entity. 


### Evaluation Criteria 

1. Ease of bringing up all services in development (use docker/docker-compose if you wish. Bonus point if you do)
2. UI/UX, bonus if work orders are shown on a [calendar](https://devexpress.github.io/devextreme-reactive/react/scheduler/)
3. Strong OOP principles 
4. Unit Tests for core logic
5. Work Order scheduled appropriately 
6. Well documented README.md 
7. SQL queries for creating all entities
8. Index added to necessary columns and data integrity constraint enforced 
9. Necessary Python APIs exposed
10. Demo/Presentation

### Technologies 

- Python/Flask 
- JavaScript/React 
- MySQL 

### Example Service 

```
id: 1
name: iPhone Screen Repair 
Duration: 2h 
-----

id: 2 
name: 3 Bedroom Apartment Full House Cleaning 
Duration: 3days
-----

id: 2
name: Dog Grooming
Duration: 4h
```

### Steps you should take 

1. Go through the requirements and let me know if you have any questions 
2. Come up with a realistic estimate of how long it will take you to get this done
3. Share your GitHub repo for the take-home with us