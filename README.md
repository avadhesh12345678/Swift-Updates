# Table of contents (Updated : Swift 4)


[#1 Build configuration import testing](https://github.com/avadhesh12345678/Swift-Updates#1-build-configuration-import-testing)
[#2 Target environment testing](https://github.com/avadhesh12345678/Swift-Updates#1-target-environment-testing)



## [#1 Build configuration import testing](https://github.com/avadhesh12345678)

```swift
#if canImport(SpriteKit)
   // this will be true for iOS, macOS, tvOS, and watchOS
#else
   // this will be true for other platforms, such as Linux
#endif
```

## [#2 Target environment testing](https://github.com/avadhesh12345678)

```swift
#if targetEnvironment(simulator)
   // code for the simulator here
#else
   // code for real devices here
#endif
```



