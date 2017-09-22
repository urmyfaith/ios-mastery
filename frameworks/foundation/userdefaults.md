

## 




## KVO the changes

Note: Do not include "." in keypath or as your identifier.

```swift

let ud = UserDefaults.standard
ud.addObserver(self, forKeyPath: "mlm_speedDelta_suddenAccel_mps", options: [.new, .initial, .old, .prior], context: &_context)

```

```swift

    override func observeValue(forKeyPath keyPath: String?, of object: Any?, change: [NSKeyValueChangeKey : Any]?, context: UnsafeMutableRawPointer?) {

```
