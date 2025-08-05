# What is MongoDB?
> MongoDB is a NoSQL, document-based database that stores data in JSON-like documents.

## How to Install MongoDB?
- You can set up MongoDB in two main ways:
| Method                       | Description                                                                                                                                                 |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Local Installation**    | Install MongoDB directly on your system (Windows, macOS, Linux). Best for development and offline projects.                                                 |
| **2. MongoDB Atlas (Cloud)** | Use MongoDB's official cloud platform — no setup needed, just sign up and start using a free cluster. Ideal for production, teamwork, and cloud deployment. |

---
## 1. Install MongoDB Locally:
- Go to: https://www.mongodb.com/try/download/community

- Download and install the MongoDB Community Edition.

- Optionally install MongoDB Compass (GUI tool).

-Start the MongoDB server using:

- `mongod`

- Use the shell or connect with Node.js/Mongoose.

## 2. Use MongoDB Atlas (Cloud):
- Go to: https://www.mongodb.com/cloud/atlas

- Sign up for free.

- Create a cluster (AWS/GCP/Azure).

- Add your IP to the whitelist and create a database user.

- Connect using a connection string (URI) in your app:
```js
mongoose.connect('mongodb+srv://username:password@cluster.mongodb.net/myDB');
```

### How to Say in Interview:
> MongoDB can be installed either locally using the Community Edition, or on the cloud using MongoDB Atlas.

## What is MongoDB Compass and MongoDB Shell?
> MongoDB provides two main tools to interact with your database:

| Tool                        | Type | Description                                                                                        |
| --------------------------- | ---- | -------------------------------------------------------------------------------------------------- |
| **MongoDB Compass**         | GUI  | A **graphical user interface** to visualize, query, and manage your data without writing commands. |
| **MongoDB Shell (mongosh)** | CLI  | A **command-line interface** to interact with MongoDB using MongoDB Query Language (MQL).          |

## Key Differences: GUI vs CLI
| Feature                 | MongoDB Compass (GUI)                   | MongoDB Shell (CLI)                         |
| ----------------------- | --------------------------------------- | ------------------------------------------- |
| **Interface**           | Graphical (point-and-click)             | Text-based (commands)                       |
| **Ease of Use**         | Beginner-friendly                       | For developers comfortable with CLI         |
| **Data Viewing**        | Browse collections visually             | Use queries to fetch data manually          |
| **Query Execution**     | Built-in query builder                  | Write MQL queries directly                  |
| **Aggregation Support** | Visual pipeline builder                 | Manual aggregation using aggregation stages |
| **Performance**         | Slightly heavier                        | Lightweight and faster                      |
| **Best For**            | Visualizing data, exploring collections | Scripting, automation, and deeper control   |

### How to Say in Interview:
> MongoDB Compass is a GUI tool that helps developers visually explore data, run queries, and manage collections without writing code. On the other hand, MongoDB Shell (mongosh) is a command-line interface used for executing queries, running scripts, and managing the database through commands.

## What is BSON and JSON in MongoDB?
| Term     | Stands For                 | Description                                                  |
| -------- | -------------------------- | ------------------------------------------------------------ |
| **JSON** | JavaScript Object Notation | A lightweight, human-readable data format.                   |
| **BSON** | Binary JSON                | A binary-encoded version of JSON used internally by MongoDB. |

## What are Query Operators in MongoDB?
> Query operators in MongoDB allow you to filter, match, and search documents based on conditions.

### Commonly Used Query Operators:
| Operator      | Type             | Description                            | Example                                                 |
| ------------- | ---------------- | -------------------------------------- | ------------------------------------------------------- |
| **`$gt`**     | Comparison       | Greater than                           | `{ age: { $gt: 18 } }`                                  |
| **`$lt`**     | Comparison       | Less than                              | `{ age: { $lt: 30 } }`                                  |
| **`$gte`**    | Comparison       | Greater than or equal to               | `{ marks: { $gte: 50 } }`                               |
| **`$lte`**    | Comparison       | Less than or equal to                  | `{ marks: { $lte: 100 } }`                              |
| **`$eq`**     | Comparison       | Equal to (default behavior if omitted) | `{ name: { $eq: "Ritesh" } }`                           |
| **`$ne`**     | Comparison       | Not equal to                           | `{ age: { $ne: 25 } }`                                  |
| **`$in`**     | Comparison       | Matches any value in an array          | `{ status: { $in: ["active", "pending"] } }`            |
| **`$nin`**    | Comparison       | Not in array                           | `{ status: { $nin: ["deleted", "blocked"] } }`          |
| **`$and`**    | Logical          | All conditions must be true            | `{ $and: [ { age: { $gt: 18 } }, { city: "Delhi" } ] }` |
| **`$or`**     | Logical          | At least one condition must be true    | `{ $or: [ { role: "admin" }, { age: { $lt: 20 } } ] }`  |
| **`$not`**    | Logical          | Negates a condition                    | `{ age: { $not: { $gt: 30 } } }`                        |
| **`$regex`**  | Pattern Matching | Matches a string pattern               | `{ name: { $regex: "^R", $options: "i" } }`             |
| **`$exists`** | Field Check      | Checks if field exists                 | `{ email: { $exists: true } }`                          |
| **`$type`**   | Type Check       | Checks the data type of a field        | `{ age: { $type: "int" } }`                             |

## What is Projection in MongoDB?
> Projection means selecting which fields to include or exclude in the result of a query.

- By default, `find()` returns all fields, but you can control it using projection syntax.
### Syntax:
```js
db.collection.find(query, projection)
```

---
### Examples:
#### 1. Include specific fields:
```js
db.users.find({ age: { $gt: 18 } }, { name: 1, age: 1 })
```
- Returns only `name` and `age` fields (and `_id` by default).
---
#### 2. Exclude specific fields:
```js
db.users.find({}, { password: 0, email: 0 })
```
- Excludes `password` and `email`.

#### 3. Hide _id:
```js
db.users.find({}, { _id: 0, name: 1 })
```
- Returns only the `name` field without `_id`.
---
