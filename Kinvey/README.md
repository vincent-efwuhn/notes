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

* Using `[KCSQuery query]` as first parameter to fetch all the items. (more about [query](http://devcenter.kinvey.com/ios/guides/datastore#Querying))


#### Update
*See Read Section*

#### Delte
`removeObject:withCompletionBlock:withProgressBlock`
* You can supply *`NSString` id*, *`NSArray` of string ids* or a *`KCSQuery` object* to delete.

### Query
Using `KCSQuery` object. ([detail](http://devcenter.kinvey.com/ios/guides/datastore#Querying))

### Relation
* **Setup** relation of objects: [link](http://devcenter.kinvey.com/ios/guides/datastore#setup)

## User
### Check Login
```objc
if ([KCSUser hasSavedCredentials] == NO) {
    //show log-in views
} else {
    //user is logged in and will be loaded on first call to Kinvey
}
```
### Facebook Login
[source](http://devcenter.kinvey.com/ios/guides/users#facebook)
