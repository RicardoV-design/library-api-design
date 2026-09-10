1. What was the most challenging part of designing this API?

- You really have to understand the flow, relationships of the resources and follow the standard status codes with correct error handling. 

2. Which endpoint was the hardest to design and why?

- Response body endpoints are the hardest to design with because it must indicate the correct status code and error message if ever the requests fails. 

3. How did you decide which operations should be nested resources vs. top-level resources?

- With the nested resources, I based it on the foreign keys so if the relation is for example 'one is to many'. Then, for the top-level resources those are the core pillars of the database. 

4. If you had to add a "Reviews" feature (users can review books), how would you design those endpoints?

- Resource: reviews

GET /api/reviews → Get all reviews  
GET /api/reviews/:id → Get 1 review by ID  
DELETE /api/reviews/:id → Delete review (Only accessible by author or admin)

**Nested Resources and Relationships**

Relationship: books has many reviews

GET /api/books/:id/reviews → Get all reviews for a specific book  
POST /api/books/:id/reviews → Create a new review for a specific book

Relationship: members has many reviews

GET /api/members/:id/reviews → Get all reviews written by a specific member

5. What is one thing you would do differently if you started over?

- I actually followed the correct process but if I will change one thing that will be on the statuses because I've assigned strings, so much better if will use strict flags. That way, it's shorter and much cleaner code. 
