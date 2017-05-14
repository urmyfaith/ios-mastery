# [Swift Standard Library](https://developer.apple.com/reference/swift)

## Types

Structs and Protocols are most thought of by people when talking about Swift Standard Libary (or API). But do not underestimate other members of this big family, such as enums, funcs, operators and typealias that they work closely together.

### [Functions](https://developer.apple.com/reference/swift/swift_standard_library_functions)

* Some funcs serve as the way to create other types.
  * One example is `stride`, and actually you cannot found the constructor for StrideThrough and StrideTo structs.
  * zip2 for Zip2Sequence
  * repeatElement for Repeated
* assertions
  * assert, assertionFailure
  * precondition, preconditionFailure
  * fatalError
* stdio
  * print, debugPrint, dump
  * readLine
* pointer-related
* numeric
  * min, max
  * numericCast


### [Operators](https://developer.apple.com/reference/swift/swift_standard_library_operators)

I found it is interesting that we can use "precedence group" to categorize these operators, which are

* Prefix (Numeric +,- , Bitwise ~, Logical !)
* Bitwise shift (Bitwise)
* Multiplication (Numeric, bit &)
* Addition (Numeric, bit | ^)
* Range formation
* Casting
* Nil coalescing
* Comparison (Numeric, Logical )
* Logical conjunction (Logical)
* Ternary
* Assignment

Besides the traditional use of operators, there are few interesting way to use operators in Swift.

* operators to construct Swift structs.
  * Range formation (..< and ...) for Ranges
* overflowing
  * &+, &-, &*


## Category of API

### Value

* Bool
* Numeric
* String
* Range
* Stride
* Pointer
* Equtable, Comparable, Hashable

### Sequence and Collection

* protocols: Sequence and Collection family
* Iterator (of Sequence) and Index (of Collection)
* structs, O(1) operation wrappers for Sequence and Collections
* structs, Slices, O(1) operation wrappers for Sequence and Collections
* Array, Dictionary , Set
* Any-prefixed type erasers
