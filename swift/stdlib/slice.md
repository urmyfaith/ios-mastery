
# Slice family (Think as SubSequence)

They are SubSequence operations of collections, which is O(1) in time.

## Instances

13 = 1 + 6*2

ArraySlice


base|Slice|Mutable*Slice
--|--|--
Collection|Slice|MutableSlice
B |BidirectionalSlice|MutableBidirectionalSlice
RA |RandomAccessSlice|MutableRandomAccessSlice
RR |RangeReplaceableSlice|MutableRangeReplaceableSlice
RRB |RangeReplaceableBidirectionalSlice|MutableRangeReplaceableBidirectionalSlice
RRRA |RangeReplaceableRandomAccessSlice|MutableRangeReplaceableRandomAccessSlice
