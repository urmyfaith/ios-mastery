

x | (Half-Opened)| Closed
--|--|--
(Uncountable) | Range | ClosedRange
Countable | CountableRange |CountableClosedRange



func ...<Bound>(minimum: Bound, maximum: Bound) -> ClosedRange<Bound> where Bound : Comparable

func ...<Bound>(minimum: Bound, maximum: Bound) -> CountableClosedRange<Bound> where Bound : Comparable, Bound : \_Strideable, Bound.Stride : SignedInteger


func ..<<Bound>(minimum: Bound, maximum: Bound) -> CountableRange<Bound> where Bound : Comparable, Bound : \_Strideable, Bound.Stride : SignedInteger

func ..<<Bound>(minimum: Bound, maximum: Bound) -> Range<Bound> where Bound : Comparable



## Refs

* https://oleb.net/blog/2016/09/swift-3-ranges/
* https://oleb.net/blog/2016/10/generic-range-algorithms/
