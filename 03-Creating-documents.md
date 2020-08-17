### Diving into Create Operations

#### Insert configuration options

##### Ordered insert

By default the insert is ordered. This cuases the operation to stop when an error like a duplicate
key happens in a batch insert.
You can modify this behaviour by passing an option in the configuration object. If you do, then
the insert will continue and not stop at the first error.
Note that this won't rollback the whole operation on failure.

![](/images/03/01.png "Ordered insert")

---

##### Atomicity

![](/images/03/02.png "Atomicity")

This means that if you insert multiple documents with _insertMany_, only those who failed in one
of their properterties will be rolled back and deemed as failed. Not the whole operation. That
is only possible with transactions.

---

##### Importing JSON data

_mongoimport_ takes the file, the database name, the collection and specify if there are multiple
documents using _jsonArray_
If _drop_ is used the data will replace documents if they already exist. Otherwise it will
be appended.

![](/images/03/03.png "Importing JSON")
