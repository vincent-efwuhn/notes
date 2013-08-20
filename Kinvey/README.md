Kinvey
====

## Basic Data Manipulation
* Declare a `KCSCollection` object to identify the collection (the scheme or object of the data).
* Declare a `KCSAppdataStore` object instance to create a data store according to the collection you want.

### CRUD
#### Create
Use `saveObject:withCompletionBlock:withProgressBlock:` to add a new record. Can supply **single object** or **`NSArray` of objects** as first parameter.

#### Read
##### Fetch by ID
`loadObjectWithID:withCompletionBlock:withProgressBlock:`
##### Fetch by Query
`queryWithQuery:withCompletionBlock:withProgressBlock:`

* Using `[KCSQuery query]` as first parameter to fetch all the items.


