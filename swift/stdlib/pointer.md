
## Pointer in Swift 3

## Why still using Pointers in Swift?

* Imported C API
* Speed
* Nature of Structs
  * Struct is copy-rule/based for assignment.
  * mutating must be specified, if applicable.
  * inheritance is not applicable for struct.

## Structs
search 'public struct', 11 results

* 2, (iterators embedded in U-(m)-R-B-P)
  * public struct Iterator : IteratorProtocol, Sequence - in UnsafeMutableRawBufferPointer
  * public struct Iterator : IteratorProtocol, Sequence - in UnsafeRawBufferPointer
* 1 UnsafeBufferPointerIterator
* 4 * 2 Pointers
  * as below

### 4 * 2 Pointers, 8 in 3D

* mutability, 4 named with prefix as `UnsafeMutable`, and 4 as `Unsafe` without followed by `Mutable`
* Raw(Bytes) vs Typed
  * 4 with `Raw` in its name
  * 4 without `Raw` but with generic
* buffer vs non-buffer - continous stored - collection
  * non-buffer, all conform to Strideable, Hashable
  * buffer. all conform to Collection, RandomAccessCollection
    * Additionally, U-B-P conform to Indexable(or MutableIndexable)

See in Table below

x | | Mutable
--|--|--
U-R-P |  UnsafeRawPointer | UnsafeMutableRawPointer
U-P | UnsafePointer\<Pointee\> | UnsafeMutablePointer\<Pointee\>
U-R-B-P	| UnsafeRawBufferPointer | UnsafeMutableRawBufferPointer
U-B-P	| UnsafeBufferPointer\<Element\> | UnsafeMutableBufferPointer\<Element\>


## Defined in Swift C module

* struct OpaquePointer : Hashable
* enum MemoryLayout\<T\>
* struct AutoreleasingUnsafeMutablePointer\<Pointee\> : Equatable


## Online Refs

* [Apple: Swift Standard Library](https://developer.apple.com/reference/swift)
* [Swift's Pointy Bits: Unsafe Swift & Pointer Types](http://news.realm.io/news/nate-cook-tryswift-tokyo-unsafe-swift-and-pointer-types)
* https://developer.apple.com/library/content/documentation/Swift/Conceptual/BuildingCocoaApps/InteractingWithCAPIs.html
