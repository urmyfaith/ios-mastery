
# Range in Swift 4

### protocol [RangeExpression](https://developer.apple.com/documentation/swift/rangeexpression)

func contains(_ element: Self.Bound) -> Bool

func relative<C>(to collection: C) -> Range<Self.Bound> where C : \_Indexable, Self.Bound == C.Index

static func ~=(pattern: Self, value: Self.Bound) -> Bool


## 4 new structs

struct | syntax | Generic Constraints
--|-- | --
[PartialRangeUpTo](https://developer.apple.com/documentation/swift/partialrangeupto) | ..<5 | Bound : Comparable
[PartialRangeThrough](https://developer.apple.com/documentation/swift/partialrangethrough) | ...5.0
[PartialRangeFrom](https://developer.apple.com/documentation/swift/partialrangefrom) | 5.0...
[CountablePartialRangeFrom](https://developer.apple.com/documentation/swift/countablepartialrangefrom) | 3... | Bound : Strideable <br>
Bound.Stride : SignedInteger


#### special on CountablePartialRangeFrom



Bound : Strideable <br>
Bound.Stride : SignedInteger

Conforms To: RangeExpression, __Sequence__

#### [UnboundedRange_](https://developer.apple.com/documentation/swift/unboundedrange-qf8)


postfix static func ...(\_: UnboundedRange_)

typealias UnboundedRange = (UnboundedRange_) -> ()

## Refs

2017/swift/604-3
