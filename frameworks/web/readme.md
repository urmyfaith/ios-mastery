
# WebKit (iOS 8), JavaScriptCore


* [JavaScriptCore](https://developer.apple.com/reference/javascriptcore)
* [WebKit](https://developer.apple.com/reference/webkit)
* http://www.joshuakehn.com/2014/10/29/using-javascript-with-wkwebview-in-ios-8.html


## [JavaScriptCore](https://developer.apple.com/reference/javascriptcore)


```swift
let js = "function add(a,b) {return a+b}"

let jsF = self.context.evaluateScript(js)!

let jsFunc =        self.context.objectForKeyedSubscript("add") as JSValue

let five = jsFunc.call(withArguments: [2, 3])!
```
