
# Range

x | (Half-Opened)| Closed
--|--|--
(Uncountable) | [`Range`](https://developer.apple.com/reference/swift/range) | [`ClosedRange`](https://developer.apple.com/reference/swift/closedrange)
Countable | [`CountableRange`](https://developer.apple.com/documentation/swift/countablerange) | [`CountableClosedRange`](https://developer.apple.com/reference/swift/countableclosedrange)

* (non-countable) range, both closed and half-opened, has much less functionality than countable counterparts.
  * Bound : Comparable
* Countable ranges can be regarded as RandomAccessCollection, for it *is*.
  * Bound : Comparable
  * Bound : \_Strideable
  * Bound.Stride : SignedInteger


## global operators to create Ranges

func ...<Bound>(minimum: Bound, maximum: Bound) -> ClosedRange<Bound> where Bound : Comparable

func ...<Bound>(minimum: Bound, maximum: Bound) -> CountableClosedRange<Bound> where Bound : Comparable, Bound : \_Strideable, Bound.Stride : SignedInteger


func ..<<Bound>(minimum: Bound, maximum: Bound) -> CountableRange<Bound> where Bound : Comparable, Bound : \_Strideable, Bound.Stride : SignedInteger

func ..<<Bound>(minimum: Bound, maximum: Bound) -> Range<Bound> where Bound : Comparable


x | where |(Half-Opened) ..<  | Closed ...
--|--|--|--
(Uncountable) | Bound : Comparable, Bound : \_Strideable, Bound.Stride : SignedInteger|
Countable |  Bound : Comparable
## Refs

* https://oleb.net/blog/2016/09/swift-3-ranges/
* https://oleb.net/blog/2016/10/generic-range-algorithms/
