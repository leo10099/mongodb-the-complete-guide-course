### Understanding the basics and core operations

#### Mongo DB Shell

##### Start process

Start mongoDB process in macOS pointing to DB folders path. It should have a parent folder named _data_ with a children called _db_ that holds the databses. It can also take an argument to change the default port (27017)

`mongod --dbpath [PATH] --port [PORT]`

---

##### See databases

`show dbs`

---

##### Switch to database

`use [name]`

---

##### BSON

- BSON is more space efficient than JSON
- Supports _ObjectId_ type
- Supports short object syntax: `insertOne({test})`

---

##### Objects Unique IDs

- You can insert a document using the _\_id_ property without relaying on mongoDB generating it but it has to be unique or mongo will throw an error.

---

##### CRUD Operations

![](/images/01.png "Crud Operations")

---

#### The Cursor object

- When performing a document search with the _find_ method mongoDB doesen't return all data. Rather, it returns a _cursor_ object with a limited set of data. It contains metada that allows to cycle through the data.

- In order to get all data in a cursor object the _toArray_ method has to be used. You can also use the _forEach_ method to perform operations on every document of the cursor.

---

#### Projection

- It simply allows to use a partial document to send only the required that the client needs.

![](/images/02.png "Projection")
