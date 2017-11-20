# RangeExpression


[`RangeExpression`](https://developer.apple.com/documentation/swift/rangeexpression)


init(uncheckedBounds bounds: (lower: Bound, upper: Bound))


x | (half-open) a..<b  | closed a...b
--|--|--
uncountable | [`Range`](https://developer.apple.com/documentation/swift/range) ..< | [`CountableClosedRange`](https://developer.apple.com/documentation/swift/countableclosedrange)
countable | [`CountableRange`](https://developer.apple.com/documentation/swift/countablerange)  |  [`CountableClosedRange`](https://developer.apple.com/documentation/swift/countableclosedrange)

countable* :  [`RandomAccessCollection`](https://developer.apple.com/documentation/swift/randomaccesscollection)

## Partials (since Swift 4)

x | from a... | through ...b | UpTo ..<b
--|--|--|--
uncountable | [`PartialRangeFrom`](https://developer.apple.com/documentation/swift/partialrangefrom) | [`PartialRangeThrough`](https://developer.apple.com/documentation/swift/partialrangethrough) | [`PartialRangeUpTo`](https://developer.apple.com/documentation/swift/partialrangeupto)
countable | [`CountablePartialRangeFrom`](https://developer.apple.com/documentation/swift/countablepartialrangefrom)


countable* :  Sequence
