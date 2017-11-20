
# Slice family (Think as SubSequence)

They are SubSequence operations of collections, which is O(1) in time.

## Instances

13 = 1 + 6 * 2

* 1 [`ArraySlice`](https://developer.apple.com/documentation/swift/arrayslice)
* 6 * 2 as below table

[`ArraySlice`](https://developer.apple.com/documentation/swift/arrayslice)

A slice of an Array, ContiguousArray, or ArraySlice instance.


base|Slice|Mutable*Slice
--|--|--
Collection|[`Slice`](https://developer.apple.com/documentation/swift/slice)|[`MutableSlice`](https://developer.apple.com/documentation/swift/mutableslice)
B |[`BidirectionalSlice`](https://developer.apple.com/documentation/swift/bidirectionalslice)|MutableBidirectionalSlice
RA |[`RandomAccessSlice`](https://developer.apple.com/documentation/swift/randomaccessslice)|MutableRandomAccessSlice
RR |[`RangeReplaceableSlice`](https://developer.apple.com/documentation/swift/rangereplaceableslice)|MutableRangeReplaceableSlice
RRB |[`RangeReplaceableBidirectionalSlice`](https://developer.apple.com/documentation/swift/rangereplaceablebidirectionalslice)|MutableRangeReplaceableBidirectionalSlice
RRRA |[`RangeReplaceableRandomAccessSlice`](https://developer.apple.com/documentation/swift/rangereplaceablerandomaccessslice)|MutableRangeReplaceableRandomAccessSlice


* https://developer.apple.com/documentation/swift/collections/supporting_types
