


```swift
enum X : Int {
 case a
 case b
}
let x = X.b

x.rawValue // in use // Risk to break, if adding `case z` before `case b`
```



* https://oleb.net/blog/2017/03/enums-equatable-exhaustiveness/



### Error: Binary operator '==' cannot be applied to two '<enum>' operands

For enum with associate values, "==" is not defined as in Int/String-backed enum. So you have to either writing switch statement or a wrapper read-only var to wrap switch statement.


https://appventure.me/2015/10/17/advanced-practical-enum-examples/
