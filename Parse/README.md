Parse
====

## Objects

### Data Types
| Types | |
|--------|----|
| `NSNumber` | `NSString` |
| `NSDate` | `NSData` |
| `NSArray` | `NSDictionary` |

> :bangbang: Not recommend store large binaray using `NSData` on `PFObject` (which need less than 128 KB). Using `PFFile` instead.



* **Get objectId** use `valueForKey:@"objectId"` of object to access. [[source](https://www.parse.com/questions/getting-objectid-always-null)]
* **Offline** use `saveEventually` and `deleteEventually`, Parse SDK will handle it. [[source](https://parse.com/docs/ios_guide#objects-offline/iOS)]


## Queries

*  `PFQuery` offers powerful ways to retrive than only using `getObjectInBackgroundWithId:block:`.

## Geo Location

* Each `PFObject` class may only have one key with a `PFGeoPoint` object.
* When the `latitude`*(-90.0,90.0)* and `longitude`*(-180.0,180.0)* out of bounts, will cause errors.

#### Advance queries
You can …

* Limit the result by using `whereKey:nearGeoPoint:withinMiles`, `whereKey:nearGeoPoint:withinKilometers`, and `whereKey:nearGeoPoint:withinRadians`.
* or limit in the geo box using `whereKey:withinGeoBoxFromSouthwest:toNortheast:`.



