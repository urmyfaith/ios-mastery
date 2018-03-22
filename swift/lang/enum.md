


```swift
enum X : Int {
 case a
 case b
}
let x = X.b

x.rawValue // in use // Risk to break, if adding `case z` before `case b`
```



* https://oleb.net/blog/2017/03/enums-equatable-exhaustiveness/


https://appventure.me/2015/10/17/advanced-practical-enum-examples/
