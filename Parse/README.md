Parse
====

## Objects

### Data Types
| Types | |
|--------|----|
| `NSNumber` | `NSString` |
| `NSDate` | `NSData` |
| `NSArray` | `NSDictionary` |

> :bangbang: Not recommend store large binaray using `NSData` on `PFObject` (which need less than 128 KB).



* **Get objectId** use `valueForKey:@"objectId"` of object to access. [[source](https://www.parse.com/questions/getting-objectid-always-null)]
* **Offline** use `saveEventually` and `deleteEventually`, Parse SDK will handle it. [[source](https://parse.com/docs/ios_guide#objects-offline/iOS)]
* 