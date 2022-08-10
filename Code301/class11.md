# Class 11 Reading Notes - Mongo and Mongoose
## NoSQL vs. SQL - The Geek Stuff
# Five Differences Between SQL and NoSQL Databases
1.  SQL databases represent data in tables with predefined schema while NoSQL databases have dynamic schema
2. SQL databases use Structured Query Language; NoSQL databases use unstructured query language and queries focus on collections of documents
3. SQL databases are much better suited for complex queries than NoSQL databases
4. SQL databases have much more support options, while NoSQL databases largely rely on community support
5. SQL databases follow ACID principles (Atomicity, Consistency, Isolation and Durability) while NoSQL  databases follow CAP(consistency, availability, partition tolerance)
# 1. What kind of data is a good fit for an SQL database?
## Relational data that can be structured into predefined schema.

# 2. Give a real world example
## A list of people and their contact information, where all the contact information is formatted the same way.

# 3. What kind of data is a good fit a NoSQL database?
## Data that doesn't fit into predefined schema (or whose schema is unknown).

# 4. Give a real world example
## A list of people with properties whose format is unknown, like a list of each of their siblings.

# 5. Which type of database is best for hierarchical data storage?
## NoSQL databases are better suited for hierarchical data storage because they can store data as key-value pairs, simiar to JSON data.

#  6. Which type of database is best for scalability?
## NoSQL databases can scale by adding more servers, giving them the opportunity to become larger and more powerful than SQL databases, which can only scale by adding capacity to the server they live on.

# SQL vs NoSQL - Academind
# 1. What does SQL stand for?
## Structured Query Language

# 2. What is a relational database?
## A database where the data is related, like a database that holds products, orders, and customer contact information. Orders will have associated products and customer information that is related to each record in the Orders table.

# 3. What type of structure does a relational database work with?
Tables

## 4. What is a ‘schema’?
The structure the data will follow, defined by fields (columns)

# 5. What is a NoSQL database?
## A collection of documents that may or may not be structured the same way and have minimal relation to each other.

# 6. How does it work?
## Instead of an order table relating to a customer table, each document in the orders collection would have all the customer info it needs.

# 7. What is inside of a Mongo database?
## Collections of Documents

# 8. Which is more flexible - SQL or MongoDB? and why
## It depends on what kind of flexibility you're looking for. MongoDB offers more scalability and doesn't require rigid schema, but SQL allows for more complex queries and handles frequent updates much more smoothly.

# 9. What is the disadvantage of a NoSQL database?
## If you are writing a lot of information to your database, you'll need to update it in every place where it's used. You also can't do queries as complex as SQL queries.

## Things I want to know more about
#### How to decide which kind of database to use early in a project, when you might not have a lot of info yet.