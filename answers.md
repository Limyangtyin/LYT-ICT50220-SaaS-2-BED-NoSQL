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
	db.movies.insertMany([
  {
    _id: ObjectId("67231930a5ec64dab72bfef3"),
    Title: "The Hobbit: An Unexpected Journey",
    Writer: "J.R.R. Tolkien",
    Year: 2012,
    Franchise: "The Hobbit",
    RunningTime: 169,
    Budget: 200000000,
    BoxOffice: 1015000000
  },
  {
    Title: "Yet Another Fake Film Name"
  },
  {
    Title: "The Hobbit: The Desolation of Smaug",
    Writer: "J.R.R. Tolkien",
    Year: 2013,
    Franchise: "The Hobbit",
    RunningTime: 161,
    Budget: 230000000,
    BoxOffice: 959300000
  },
  {
    Title: "Inglorious Basterds",
    Writer: "Quentin Tarantino",
    Year: 2009,
    Actors: ["Brad Pitt", "Diane Kruger", "Eli Roth"],
    RunningTime: 153,
    Budget: 70000000,
    BoxOffice: 321500000
  },
  {
    Title: "Star Trek: Nemesis",
    Year: 2002,
    Writer: ["John Logan", "Rick Berman", "Brent Spiner"],
    Summary: "A clone of Picard, created by the Romulans, assassinates the Romulan Senate, assumes absolute power, and lures Picard and the Enterprise to Romulus under the false pretext of a peace overture.",
    Franchise: "Star Trek",
    RunningTime: 117,
    Budget: 60000000,
    BoxOffice: 67300000
  },
  {
    Title: "Avatar"
  },
  {
    Title: "Pee Wee Herman's Big Adventure",
    RunningTime: 91,
    Budget: 7000000,
    BoxOffice: 40900000
  },
  {
    Title: "Pulp Fiction",
    Writer: "Quentin Tarantino",
    Year: 1994,
    Actors: ["John Travolta", "Uma Thurman"],
    RunningTime: 154,
    Budget: 8000000,
    BoxOffice: 213900000
  },
  {
    Title: "Dummy Film Name"
  },
  {
    Title: "The Hobbit: The Battle of the Five Armies",
    Writer: "J.R.R. Tolkien",
    Year: 2012,
    Franchise: "The Hobbit",
    Synopsis: "Bilbo and Company are forced to engage in a war against an array of combatants and keep the Lonely Mountain from falling into the hands of a rising darkness.",
    RunningTime: 144,
    Budget: 250000000,
    BoxOffice: 940300000
  },
  {
    Title: "Another Fictional Film Name"
  },
  {
    Title: "Star Trek VI: The Undiscovered Country",
    Year: 1991,
    Franchise: "Star Trek",
    Writer: ["Nicholas Meyer", "Denny Martin Flinn"],
    Summary: "When Qo'noS' moon Praxis (the Klingon Empire's chief energy source) is devastated by an explosion, caused by over-mining, the catastrophe also contaminating Qo'noS' atmosphere, the Klingons make peace overtures to the Federation. While on the way to Earth for a peace summit, the Klingon Chancellor is assassinated by Enterprise crewmen, and Kirk and McCoy are held accountable by the Chancellor's Chief of Staff and sentenced to life on a prison planet. Spock attempts to prove Kirk's innocence, but in doing so, uncovers a massive conspiracy against the peace process with participants from both sides.",
    RunningTime: 110,
    Budget: 30000000,
    BoxOffice: 96800000
  }
]);

```

# Step 5: CRUD - Retrieve Queries

## 5.1 Retrieve all documents

- Get all documents

Query Solution:

```js
	db.movies.find();
```
	
## 5.2 Retrieve all films written by…

- Get all documents with `writer` set to "Quentin Tarantino"

Query Solution:

```js
	db.movies.find({Writer: "Quentin Tarantino"});
```

Screen Shot:

![NoSQL Databases & Collection](./images/step-5.2-001.png)

## 5.3 Retrieve films with actor(s)…

- Get all documents where `actors` include "Brad Pitt"

Query Solution:

```js
	db.movies.find({Actors: "Brad Pitt"});
```
	
## 5.4 Retrieve films from a franchise…

- Get all documents with `franchise` set to "The Hobbit"

Query Solution:

```js
	db.movies.find({Franchise: "The Hobbit"});
```
	
## 5.5 Retrieve films before/after…

- Get all movies released before 1995 or after 2010 

Query Solution:

```js
	db.movies.find({
		$or: [
			{Year: {$lt: 1995}},
			{Year: {$gt: 2010}}
		]
	});
```
	
Screen Shot:

![NoSQL Databases & Collection](./images/step-5.5-001.png)
![NoSQL Databases & Collection](./images/step-5.5-002.png)
![NoSQL Databases & Collection](./images/step-5.5-003.png)


## 5.6 Retrieve films longer than…

- Get all movies with a running time of over 100 minutes

Query Solution:

```js
	db.movies.find({ RunningTime: { $gt: 100}});
```

# Step 6: CRUD - Updates

## 6.1 Update document with a synopsis

- Using one or more queries, add the following synopses to the indicated movies:

Query Solution:

```js
	db.movies.updateOne(
  { Title: "The Hobbit: The Desolation of Smaug" },
  { $set: { Synopsis: "The dwarves, along with Bilbo Baggins and Gandalf the Grey, continue their quest to reclaim Erebor, their homeland, from Smaug. Bilbo Baggins is in possession of a mysterious and magical ring." } }
);

db.movies.updateOne(
  { Title: "The Hobbit: An Unexpected Journey" },
  { $set: { Synopsis: "A reluctant hobbit, Bilbo Baggins, sets out to the Lonely Mountain with a spirited group of dwarves to reclaim their mountain home - and the gold within it - from the dragon Smaug." } }
);
```
	
## 6.2 Update document with an actor

- Add the following actors to the indicated films using one or more queries in the order provided...

Query Solution:

```js
	db.movies.updateOne(
		{Title: "Star Trek VI: The Undiscovered Country"},
		{$addToSet: {Actors: {$each: ["William Shatner", "Leonard Nimoy", "Deforest Kelly", "James Doohan", "Christopher Plummer"]}}}
	);

	db.movies.updateOne(
		{Title: "Star Trek: Nemesis"},
		{$addToSet: {Actors: {$each: ["Patrick Stewart", "Jonathan Frakes", "Brent Spiner", "LeVar Burton", "Michael Dorn", "Gates McFadden", "Marina Sirtis" ]}}}
	);

	db.movies.updateOne(
		{Title: "Star Trek VI: The Undiscovered Country"},
		{$addToSet: {Actors: {$each: ["Walter Koenig", "Nichelle Nochols", "George Takei", "Kim Cattrall", "David Warner"]}}}
	);
```

Screen Shot:

![NoSQL Databases & Collection](./images/step-6.2-001.png)
![NoSQL Databases & Collection](./images/step-6.2-002.png)
![NoSQL Databases & Collection](./images/step-6.2-003.png)
![NoSQL Databases & Collection](./images/step-6.2-004.png)

# Step 7: CRUD – Searches

Performing searches on collections.

## 7.1 Searching for titles with …

- Find all movies with "F" in the title.

Query Solution:

```js
	db.movies.find(
		{Title: {$regex: /F/i}}
	);
```

## 7.2 Searching for synopses with …

- Find all movies that have a synopsis that contains the word "Gandalf"

Query Solution:

```js
	db.movies.find(
		{Title: {$regex: /Gandalf/i}}
	);
```

## 7.3 Searching for synopses with… and not …

- Find all movies that have a synopsis that contains the word "Bilbo" and not the word "Gandalf"

Query Solution:

```js
	db.movies.find(
		{Synopsis: {$regex: /Bilbo/i, $not: /Gandalf/i}}
	);
```

## 7.4 Searching for synopses with … or …

- Find all movies that have a synopsis that contains the word "Klingon" or "Romulan"

Query Solution:

```js
	db.movies.find(
		{
			Synopsis: {
				$regex: /Klingon|Romulan/i
			}
		}
	);
```

Screen Shot:

![NoSQL Databases & Collection](./images/step-7.4-001.png)

## 7.5 Searching for synopses with … and …

- Find all movies that have a synopsis that contains the words "gold" and "dragon"

Query Solution:

```js
	db.movies.find(
		{
			Synopsis: {
				$regex: /Gold/i, $regex: /Dragon/i
			}
		}
	);
```

# Step 8: CRUD - Deletions

This step requires you to remove movies from the collection.

## 8.1 Removing a movie using its title…

- Delete the movie "Pee Wee Herman's Big Adventure"

Query Solution:

```js
db.movies.deleteOne({Title: "Pee Wee Herman's Big Adventure"});

```

Screen Shot:

![NoSQL Databases & Collection](./images/step-8.1-001.png)

## 8.2 Remove a movie by ID…

- Discovering its ID, Then using the ID to remove the movie

Query Solution:

```js
	db.movies.find({Title: "Yet Another Fake Film Name"});

  db.movies.deleteOne({_id: ObjectId('671a043e9aff4f5ffd6bcfad')});

```

## 8.3 Removing multiple movies…

- Delete any movies with “Fiction” in their title

Query Solution:

```js
	db.movies.deleteMany({Title: /Fiction/i});
```

# Step 9: NoSQL Indexes

Using the movies collection, create the indexes to match the following conditions

## 9.1 Indexing a single field

- Create an index on the `title` field.

Query Solution:

```js
	db.movies.createIndex({Title: 1});
```

Screen Shot:

![NoSQL Databases & Collection](./images/step-9.1-001.png)

## 9.2 Indexing multiple fields

- Create a text index on the `title ` and `franchise` fields.

Query Solution:

```js
	db.movies.createIndex({Title: 'text', Franchise: 'text'});

  db.movies.createIndex({Franchise: 1, Title: 1});
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

