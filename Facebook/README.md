Facebook
====

## Login call back
(ref: [source](https://developers.facebook.com/docs/tutorials/ios-sdk-tutorial/authenticate/#step2))

```objc
- (BOOL)application:(UIApplication *)application 
            openURL:(NSURL *)url
  sourceApplication:(NSString *)sourceApplication 
         annotation:(id)annotation 
{
    return [FBSession.activeSession handleOpenURL:url]; 
}
```

**Permission** to post feed

```
publish_stream
```
……
