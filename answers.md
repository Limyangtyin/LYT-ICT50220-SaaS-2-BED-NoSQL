---
updated: 2024-10-24T00:16
created: 2024-10-23T21:09
---
# Answers

## Software as a Service - Back-End Development

### Diploma of Information Technology (Advanced Programming)  

### Diploma of Information Technology (Back-End Development)

Complete this table with the required information, then remove this line:

| Given Name | Family Name | Student ID |
| -----Yang Tyin----- | -----Lim----- | -----20103962----- |
|            |             |            |


---
```table-of-contents
title: # Contents
style: nestedList
minLevel: 0
maxLevel: 3
includeLinks: true
```

---

# Answers

By completing this document, and the associated MS Word Document, you agree that the work is yours....

# How to Answer Questions

Each time you answer a question, fill out the space provided for the answer to the question.

```text
## Question X - Title

Query Solution:

```js
	db.collection_name.find();
	```
```

The NoSQL code used to answer the question is contained in a code block, as shown above. 

It is important that code blocks start at the beginning of the line for formatting on GitHub, Obsidian or your preferred IDE render the code correctly.

Images are embedded using the following syntax:

```markdown
![Short Image Title](./folder/filename.extension)
```

For example:

```markdown
![Embedding an Image Example](./assets/step-N-XXX.png)
```

Gives:

![Embedding an Image Example](assets/step-N-XXX.png)


# Step 2: NoSQL Systems

## 2.1 Identify Data Types

| Item | Data Type     |
|---------|---------------|
| id  | ObjectId      |
| title | string        |
| year | integer       |
| writer | array(string) | 
| summary | string        | 
| franchise | string        | 
| running time | integer       |
| budget | integer       |
| box office | double        | 



# Step 3: NoSQL Databases & Collections

## 3.1 Connecting

- Connect to a running instance of MongoDB (this may be local or in the cloud).

Connection String:

```js
	mongodb://localhost:27017
```
	
### 3.2 Database Creation

- Create and use a database named `saas_bed_portfolio_2024s2`.

Query Solution:

```js
	use saas_bed_portfolio_2024s2
```

### 3.3 Collection Creation

- Create a new collection named movies and insert ...

Query Solution:

```js
	db.createCollection('movies')
    db.movies.insertOne({Title: 'Fight Club', Writer: 'Chuck Palahniuk', Year: 1999, Actors: ['Brad Pitt', 'Edward Norton']})
```

Screen Shot:

![NoSQL Databases & Collection](./images/step-3-001.png)

# Step 4: CRUD - Create

## 4.1 Inserting Data

- Using between TWO and FOUR statements, add the following data into the movies collection in the order provided. 

Query Solution:

```js
	db.collection_name.find();
```

# Step 5: CRUD - Retrieve Queries

## 5.1 Retrieve all documents

- Get all documents

Query Solution:

```js
	db.collection_name.find();
```
	
## 5.2 Retrieve all films written by…

- Get all documents with `writer` set to "Quentin Tarantino"

Query Solution:

```js
	db.collection_name.find();
```

Screen Shot:

> Replace this line with a screenshot of the output from the writer query.

## 5.3 Retrieve films with actor(s)…

- Get all documents where `actors` include "Brad Pitt"

Query Solution:

```js
	db.collection_name.find();
```
	
## 5.4 Retrieve films from a franchise…

- Get all documents with `franchise` set to "The Hobbit"

Query Solution:

```js
	db.collection_name.find();
```
	
## 5.5 Retrieve films before/after…

- Get all movies released before 1995 or after 2010 

Query Solution:

```js
	db.collection_name.find();
```
	
Screen Shot:

> Replace this line with a screenshot of the output from the range query.

## 5.6 Retrieve films longer than…

- Get all movies with a running time of over 100 minutes

Query Solution:

```js
	db.collection_name.find();
```

# Step 6: CRUD - Updates

## 6.1 Update document with a synopsis

- Using one or more queries, add the following synopses to the indicated movies:

Query Solution:

```js
	db.collection_name.find();
```
	
## 6.2 Update document with an actor

- Add the following actors to the indicated films using one or more queries in the order provided...

Query Solution:

```js
	db.collection_name.find();
```

Screen Shot:

> Replace this line with a screenshot of the output from the update query.

# Step 7: CRUD – Searches

Performing searches on collections.

## 7.1 Searching for titles with …

- Find all movies with "F" in the title.

Query Solution:

```js
	db.collection_name.find();
```

## 7.2 Searching for synopses with …

- Find all movies that have a synopsis that contains the word "Gandalf"

Query Solution:

```js
	db.collection_name.find();
```

## 7.3 Searching for synopses with… and not …

- Find all movies that have a synopsis that contains the word "Bilbo" and not the word "Gandalf"

Query Solution:

```js
	db.collection_name.find();
```

## 7.4 Searching for synopses with … or …

- Find all movies that have a synopsis that contains the word "Klingon" or "Romulan"

Query Solution:

```js
	db.collection_name.find();
```

Screen Shot:

> Replace this line with a screenshot of the output from the synopses search.

## 7.5 Searching for synopses with … and …

- Find all movies that have a synopsis that contains the words "gold" and "dragon"

Query Solution:

```js
	db.collection_name.find();
```

# Step 8: CRUD - Deletions

This step requires you to remove movies from the collection.

## 8.1 Removing a movie using its title…

- Delete the movie "Pee Wee Herman's Big Adventure"

Query Solution:

```js
	db.collection_name.find();
```

Screen Shot:

> Replace this line with a screenshot of the output from the delete query.

## 8.2 Remove a movie by ID…

- Discovering its ID, Then using the ID to remove the movie

Query Solution:

```js
	db.collection_name.find();
```

## 8.3 Removing multiple movies…

- Delete any movies with “Fiction” in their title

Query Solution:

```js
	db.collection_name.find();
```

# Step 9: NoSQL Indexes

Using the movies collection, create the indexes to match the following conditions

## 9.1 Indexing a single field

- Create an index on the `title` field.

Query Solution:

```js
	db.collection_name.find();
```

Screen Shot:

> Replace this line with a screenshot of the output from the creation index.

## 9.2 Indexing multiple fields

- Create a text index on the `title ` and `franchise` fields.

Query Solution:

```js
	db.collection_name.find();
```


## 9.3 Verifying execution plans

- Check the execution plan for a query that finds the movies with a title containing “Star”. Check if the created index is being used.

Query Solution:

```js
	db.collection_name.find();
```

Screen Shot:

> Replace this line with a screenshot of the output from the execution plan.

# Step 10: Aggregation

In this step you will be aggregating data within a collection.

## 10.1 Counting documents

- Write the query to count the number of Star Trek movies.

Query Solution:

```js
	db.collection_name.find();
```

## 10.2 Mean box office takings…

- Write the query to calculate the average box office earnings.

Query Solution:

```js
	db.collection_name.find();
```

## 10.3 Profit earnings

- Write a query to calculate the profit (box office – budget) for the movies, showing just the movie title and the profit.

Query Solution:

```js
	db.collection_name.find();
```

Screen Shot:

> Replace this line with a screenshot of the output from the profit calculation query.

## 10.4 Grouping data

- Write the query to group movies by their franchise and count the number of movies in each franchise.

Query Solution:

```js
	db.collection_name.find();
```

# Step 11: Triggers

Using the movies collection, we are now going to create triggers to provide an audit trail for when data is added, updated or deleted.

## 11.1 Create trigger for inserted data

- Create a trigger that monitors the movies collection for new data being added. 

Query Solution:

```js
	db.collection_name.find();
```

## 11.2 Testing the insert trigger works correctly

- Use the following data to check the trigger functions as expected:

Query Solution:

```js
	db.collection_name.find();
```

## 11.3 Create trigger for updated data

- Create a trigger that monitors the movies collection for new data being added. 

Query Solution:

```js
	db.collection_name.find();
```

Screen Shot:

> Replace this line with a screenshot of the output from the creation of the trigger.

## 11.4 Testing the update trigger works correctly

- Use the following data to verify that the trigger functions as expected. Make sure that these updates are completed in more than one query:

Query Solution:

```js
	db.collection_name.find();
```

## 11.5 Create trigger for deleted data

- Create a trigger that monitors the movies collection for new data being added. 

Query Solution:

```js
	db.collection_name.find();
```

## 11.6 Testing the delete trigger works correctly

- Use the following conditions to verify that the trigger functions as expected:

Query Solution:

```js
	db.collection_name.find();
```

## 11.7 Verify the log contains data…

- Write a query to show the data in the movie audit log.

Query Solution:

```js
	db.collection_name.find();
```

Screen Shot:

> Replace this line with a screenshot of the output from the movie audit log.



# Step 12: Submission

What is the URL for your GitHub (or equivalent) repository for this assessment?

```text
add url here
```

# END

