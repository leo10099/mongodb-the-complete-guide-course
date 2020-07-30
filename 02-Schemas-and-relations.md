### Schemas and relations - How to structure data

---

##### Data Types

![](/images/02/01.png "Data Types")
![](/images/02/02.png "Using all data types")

---

##### Nested VS References

- It is recommended to use nested documents only when the data doesen't change as much and when the nested data is tightly coupled. For example, considerate how you fetch data of this entity: if you often request the
  nested document alone frequently. If so then a reference approach is more
  convenient.

![](/images/02/03.png "Nested vs References")

![](/images/02/04.png "Nested vs References - When to use each")

---

#### Joining with lookup operation

- Getting related data in one step merged together

![](/images/02/05.png "$lookup")
