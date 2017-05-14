


## Sequence and Collection family

* Sequence
  * Collection
    * MutableCollection
    * RangeReplaceableCollection \[ | [SwiftDoc](http://swiftdoc.org/v3.1/protocol/RangeReplaceableCollection/) | \]
    * BidirectionalCollection
      * RandomAccessCollection \[[Apple](https://developer.apple.com/reference/swift/randomaccesscollection) | [SwiftDoc](http://swiftdoc.org/v3.1/protocol/RandomAccessCollection/) | [GitHub] \]



## O(1) operation (wrapper) around Sequence and Collection family


prefix | Sequence | Iterator | Collection | Index | Collection++
--|--|--|--|--|--
Lazy (#4)|Y | |LazyCollection|  | LazyBidirectionalCollection LazyRandomAccessCollection
LazyFilter (#5)|Y|Y|Y|Y| LazyFilterBidirectionalCollection
LazyMap (#5)| LazyMapSequence |LazyMapIterator|LazyMapCollection| | LazyMapBidirectionalCollection  LazyMapRandomAccessCollection
LazyDropWhile (#5)|
LazyPrefixWhile (#5)|||||
Flatten|
Slice (#6)|
Mutable*Slice (#6)|
Reversed (#4)| | | ReversedCollection | ReversedIndex ReversedRandomAccessIndex | ReversedRandomAccessCollection
Any|


## Refs

* [realm.io: Everything You Ever Wanted To Know About Sequence and Collection](http://news.realm.io/news/try-swift-soroush-khanlou-sequence-collection)
* https://oleb.net/blog/2017/02/why-is-dictionary-not-a-mutablecollection/
