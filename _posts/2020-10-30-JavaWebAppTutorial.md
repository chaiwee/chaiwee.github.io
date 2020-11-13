---
layout: post
title: MVC Architecture in Java
---

In web development, MVC is one of the most talked design pattern

## Three topics to understand MVC:
1. What is MVC?
2. Advantages?
3. Implementation in Java

## Notes:  
- Design Pattern: A technique to solve a commonly occuring problem when designing software.  
- Design Model: Specifies what type of architecture you use to solve problem or design model  
- 2 types design model: Model 1 Architecture, Model 2(MVC) Architecture  

### 1. What is MVC?  
Model - the business layer  
View - the presentation  
Controller - manages the flow  
DAO - data access object, if you create one DAO class for each DB table, maintainence becomes easier
VO - columns in a DB table are created as member variables, and the column values of the table are used to treat the column values as objects in java (data is encapsulated and made into an object)
(source: https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/08/MVC-1-768x306.png)  

### 2. Advantages  
- multiple developers work simultaneously on the three layers  
- scalability  
- low dependency on each other  
- reusablity of model in views  
- testing and extending becomes easy  
  
### 3. Implementations  
(a) Model Layer - consists functions of getter and setter  
(b) View Layer - represent output of the app or the user interface  
               - display data fetch from model by controller to user  
               - doesnt need to interact with model directly  
(c) Controller Layer - an interface between model and view  
                     - receive user request from view, process them, send to model for data processing, then display in view again  
