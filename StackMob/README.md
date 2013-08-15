StackMob
===========

* If ther are some field not plaing to interacting with to the client, *don't* include in the models in Xcode.

### Upload binary
**Tutorial** [[link](https://developer.stackmob.com/ios-sdk/upload-files-to-s3-tutorial)]

~~:interrobang: cannot set binary field in schema.~~ It worked eventually.

* **Binary field:** Add binary field in th schema you want.
* **Xcode model:** Add a field as type String, StackMob will return S3 url.