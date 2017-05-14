

## Equtable [Apple](https://developer.apple.com/reference/swift/equatable) | [SwiftDoc](http://swiftdoc.org/v3.1/protocol/Equatable/)

## Hashable [Apple](https://developer.apple.com/reference/swift/hashable) | [SwiftDoc](http://swiftdoc.org/v3.1/protocol/Hashable/) | [GitHub](https://github.com/apple/swift/blob/master/stdlib/public/core/Hashable.swift)

```swift
public protocol Hashable : Equatable {
    public var hashValue: Int { get }
}
```

### How to implement Hashable

By the way, the worst case, is you got O(N).?

Refs

* http://iamsim.me/swift-equatable-and-hashable/
* http://samuelmullen.com/2014/10/implementing_swifts_hashable_protocol/
* https://useyourloaf.com/blog/swift-hashable/
