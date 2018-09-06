# Table of contents (Updated : Swift 4)


[#1 Build configuration import testing](https://github.com/avadhesh12345678/Swift-Updates#1-build-configuration-import-testing)         
[#2 Target environment testing](https://github.com/avadhesh12345678/Swift-Updates#2-target-environment-testing)     
[#3 Derived collections of enum cases](https://github.com/avadhesh12345678/Swift-Updates#3-derived-collections-of-enum-cases)     
[#4 Warning and error diagnostic directives](https://github.com/avadhesh12345678/Swift-Updates#4-warning-and-error-diagnostic-directives)       
[#5 Random number generation and shuffling](https://github.com/avadhesh12345678/Swift-Updates#5-random-number-generation-and-shuffling)  
[#6 Boolean toggling](https://github.com/avadhesh12345678/Swift-Updates#6-boolean-toggling)
[#7 In-place collection element removal](https://github.com/avadhesh12345678/Swift-Updates#7-in-place-collection-element-removal) 



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

## [#3 Derived collections of enum cases](https://github.com/avadhesh12345678)

```swift
enum Developers: CaseIterable {
    case vishal, avadhesh, sandeep, anil
}
```
```swift
for developer in Developers.allCases {
    print("iOS Developer - \(developer).")
}
```
```swift

```

## [#4 Warning and error diagnostic directives](https://github.com/avadhesh12345678)

```swift
func encrypt(_ string: String, with password: String) -> String {
    #warning("This is terrible method of encryption")
    return password + String(string.reversed()) + password
}

struct Configuration {
    var apiKey: String {
        #error("Please enter your API key below then delete this line.")
        return "Enter your key here"
    }
} 
```


## [#5 Random number generation and shuffling](https://github.com/avadhesh12345678)

```swift
let randomInt = Int.random(in: 1..<5)

Similar methods exist for Float, Double, and CGFloat:

let randomFloat = Float.random(in: 1..<10)
let randomDouble = Double.random(in: 1...100)
let randomCGFloat = CGFloat.random(in: 1...1000)
```

## [#6 Boolean toggling](https://github.com/avadhesh12345678)

```swift
var loggedIn = false
loggedIn.toggle()
```

## [#7 In-place collection element removal](https://github.com/avadhesh12345678)

```swift
var developers = ["Avadhesh", "Vishal", "Sandeep", "Anil", "Prashant"]
developers.removeAll { $0.hasPrefix("Sandeep") }
print(developers)
```









