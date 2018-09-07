# Table of contents 




# Swift 4.2 Updates


[#8 Build configuration import testing](https://github.com/avadhesh12345678/Swift-Updates#8-build-configuration-import-testing)         
[#7 Target environment testing](https://github.com/avadhesh12345678/Swift-Updates#7-target-environment-testing)     
[#6 Derived collections of enum cases](https://github.com/avadhesh12345678/Swift-Updates#6-derived-collections-of-enum-cases)     
[#5 Warning and error diagnostic directives](https://github.com/avadhesh12345678/Swift-Updates#5-warning-and-error-diagnostic-directives)       
[#4 Random number generation and shuffling](https://github.com/avadhesh12345678/Swift-Updates#4-random-number-generation-and-shuffling)  
[#3 Boolean toggling](https://github.com/avadhesh12345678/Swift-Updates#3-boolean-toggling)  
[#2 In-place collection element removal](https://github.com/avadhesh12345678/Swift-Updates#2-in-place-collection-element-removal)  
[#1 Checking sequence elements match a condition](https://github.com/avadhesh12345678/Swift-Updates#1-checking-sequence-elements-match-a-condition)   


## [#8 Build configuration import testing](https://github.com/avadhesh12345678)

```swift
#if canImport(SpriteKit)
   // this will be true for iOS, macOS, tvOS, and watchOS
#else
   // this will be true for other platforms, such as Linux
#endif
```

## [#7 Target environment testing](https://github.com/avadhesh12345678)

```swift
#if targetEnvironment(simulator)
   // code for the simulator here
#else
   // code for real devices here
#endif
```

## [#6 Derived collections of enum cases](https://github.com/avadhesh12345678)

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

## [#5 Warning and error diagnostic directives](https://github.com/avadhesh12345678)

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


## [#4 Random number generation and shuffling](https://github.com/avadhesh12345678)

```swift
let randomInt = Int.random(in: 1..<5)

Similar methods exist for Float, Double, and CGFloat:

let randomFloat = Float.random(in: 1..<10)
let randomDouble = Double.random(in: 1...100)
let randomCGFloat = CGFloat.random(in: 1...1000)
```

## [#3 Boolean toggling](https://github.com/avadhesh12345678)

```swift
var loggedIn = false
loggedIn.toggle()
```

## [#2 In-place collection element removal](https://github.com/avadhesh12345678)

```swift
var developers = ["Avadhesh", "Vishal", "Sandeep", "Anil", "Prashant"]
developers.removeAll { $0.hasPrefix("Sandeep") }
print(developers)
```

## [#1 Checking sequence elements match a condition](https://github.com/avadhesh12345678)

```swift
let scores = [80, 88, 95, 92]
let passed = scores.allSatisfy { $0 >= 85 }
```









