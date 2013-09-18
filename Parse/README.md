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

### Subclassing PFObject
You can *declare your own methods* to do more complicated logic.
further see [subclasses](https://www.parse.com/docs/ios_guide#subclasses/iOS)

#### Original:

```objc
PFObject *shield = [PFObject objectWithClassName:@"Armor"];
[shield setObject:@"Wooden Shield" forKey:@"displayName"];
[shield setObject:[NSNumber numberWithBool:NO] forKey:@"fireProof"];
[object setObject:[NSNumber numberWithInt:50] forKey:@"rupees"];
```

#### After:

```objc
Armor *shield = [Armor object];
shield.displayName = @"Wooden Shield";
shield.fireProof = NO;
shield.rupees = 50;
```


## Queries

*  `PFQuery` offers powerful ways to retrive than only using `getObjectInBackgroundWithId:block:`.

## Geo Location

* Each `PFObject` class may only have one key with a `PFGeoPoint` object.
* When the `latitude`*(-90.0,90.0)* and `longitude`*(-180.0,180.0)* out of bounts, will cause errors.

#### Advance queries
You can …

* Limit the result by using `whereKey:nearGeoPoint:withinMiles`, `whereKey:nearGeoPoint:withinKilometers`, and `whereKey:nearGeoPoint:withinRadians`.
* or limit in the geo box using `whereKey:withinGeoBoxFromSouthwest:toNortheast:`.

## User
* Sign up
* Login

### Roles

using the `PFRole` Object - implement ACLs
class doc -> [`PFRole`](https://www.parse.com/docs/osx/api/Classes/PFRole.html)

## IAP

to setup in-app-purchase, see [guide](https://developer.apple.com/library/ios/technotes/tn2259/_index.html) from apple.


