### Understanding the basics and core operations

#### Mongo DB Shell

##### 1. Start process

Start mongoDB process in macOS pointing to DB folders path. It should have a parent folder named _data_ with a children called _db_ that holds the databses. It can also take an argument to change the default port (27017)

`mongod --dbpath [PATH] --port [PORT]`

---

##### 2. See databases

`show dbs`

---

##### 3. Switch to database

`use [name]`

---

##### 4. BSON

- BSON is more space efficient than JSON
- Supports _ObjectId_ type
- Supports short object syntax: `insertOne({test})`

---

##### 5. Objects Unique IDs

- You can insert a document using the _\_id_ property without relaying on mongoDB generating it but it has to be unique or mongo will throw an error.

---

##### 6. CRUD Operations

[crud]: ("/images/01.png")
